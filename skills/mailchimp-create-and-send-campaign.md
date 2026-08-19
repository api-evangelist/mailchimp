---
name: Create, populate, check, and send a Mailchimp campaign
description: Build a regular email campaign against an audience, set its HTML content, run the pre-send checklist, send a test, then send or schedule it.
api: openapi/mailchimp-campaigns-api-openapi.yml
generated: '2026-08-13'
method: generated
source: >-
  Grounded in operationIds verified in openapi/mailchimp-marketing-api-openapi-original.json
  (Mailchimp Marketing API 3.0.91, harvested 2026-08-13); mirrors
  arazzo/mailchimp-create-campaign-set-content-send-workflow.yml.
operations:
  - getLists
  - postCampaigns
  - putCampaignsIdContent
  - getCampaignsIdSendChecklist
  - postCampaignsIdActionsTest
  - postCampaignsIdActionsSend
  - postCampaignsIdActionsSchedule
  - getCampaignsId
---

# Create and send a Mailchimp campaign

Sending is **irreversible and has real-world consequence** — it delivers mail to
real people. Treat `postCampaignsIdActionsSend` as a human-in-the-loop step
(`agentic-access/mailchimp-agentic-access.yml`).

## Steps

1. `getLists` — `GET /lists` — resolve the audience `id` to send to.
2. `postCampaigns` — `POST /campaigns` — create the campaign:
   ```json
   {
     "type": "regular",
     "recipients": { "list_id": "<list_id>" },
     "settings": {
       "subject_line": "…",
       "title": "…",
       "from_name": "…",
       "reply_to": "…"
     }
   }
   ```
   Keep the returned `id`. **Do not retry a failed create blindly** — there is no
   idempotency key, so a retry after a timeout can create a second draft. Instead
   `GET /campaigns?count=…` and look for your `settings.title` before retrying.
3. `putCampaignsIdContent` — `PUT /campaigns/{campaign_id}/content` — set `html`,
   or `template: {id, sections}` when rendering from a template. This is a full
   replace and is safe to repeat.
4. `getCampaignsIdSendChecklist` — `GET /campaigns/{campaign_id}/send-checklist` —
   Mailchimp's own pre-send validation. **Stop if any item has
   `type: "error"`.** This is the cheapest guard an agent has before an
   irreversible send.
5. `postCampaignsIdActionsTest` — `POST /campaigns/{campaign_id}/actions/test` —
   `{"test_emails":["…"],"send_type":"html"}`. Send to an internal address first.
6. Then either:
   - `postCampaignsIdActionsSend` — `POST /campaigns/{campaign_id}/actions/send` —
     sends immediately. Returns `204` with no body. **Requires human approval.**
   - `postCampaignsIdActionsSchedule` — `POST /campaigns/{campaign_id}/actions/schedule` —
     `{"schedule_time":"<ISO 8601 UTC>"}`. Mailchimp only accepts times on the
     quarter hour (`:00`, `:15`, `:30`, `:45`).
7. `getCampaignsId` — `GET /campaigns/{campaign_id}` — confirm `status`
   (`save` → `schedule` → `sending` → `sent`).

## Rules an agent must follow

- A campaign cannot be sent twice; a repeated send returns an error, not a duplicate.
  Read `status` before retrying anything after step 6.
- `postCampaignsIdActionsReplicate` (`POST /campaigns/{campaign_id}/actions/replicate`)
  is the correct way to reuse a sent campaign — never mutate a sent one.
- Reporting lands on `getReportsId` (`GET /reports/{campaign_id}`) minutes after
  the send; see `skills/mailchimp-pull-campaign-report.md`.
- Errors are `application/problem+json`; 10-connection concurrency limit and
  `429`/`403` throttling apply to every call above.
