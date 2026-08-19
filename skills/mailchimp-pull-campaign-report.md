---
name: Pull a Mailchimp campaign report
description: Find a sent campaign and read its report — aggregate performance, per-recipient email activity, opens and clicks — without exhausting the 10-connection limit.
api: openapi/mailchimp-reports-api-openapi.yml
generated: '2026-08-13'
method: generated
source: >-
  Grounded in operationIds verified in openapi/mailchimp-marketing-api-openapi-original.json
  (Mailchimp Marketing API 3.0.91, harvested 2026-08-13); mirrors
  arazzo/mailchimp-find-campaign-pull-report-workflow.yml.
operations:
  - getCampaigns
  - getReportsId
  - getReportsIdEmailActivity
  - getReportsIdClickDetails
  - getReportsIdOpenDetails
  - getReportsIdSentTo
---

# Pull a Mailchimp campaign report

Read-only. Safe to run unattended — but the report endpoints are the most
expensive in the API and the ones most likely to hit the 120-second timeout.

## Steps

1. `getCampaigns` — `GET /campaigns?status=sent&sort_field=send_time&sort_dir=DESC`
   — find the campaign `id`. Narrow the payload with
   `fields=campaigns.id,campaigns.settings.subject_line,campaigns.send_time,total_items`.
2. `getReportsId` — `GET /reports/{campaign_id}` — the aggregate report:
   `emails_sent`, `opens` (`opens.opens_total`, `unique_opens`, `open_rate`),
   `clicks`, `bounces`, `unsubscribed`, `list_stats`.
   Report data lags the send by minutes; a report fetched immediately after
   `actions/send` will be near-zero and is not an error.
3. Detail, only when you need it:
   - `getReportsIdEmailActivity` — `GET /reports/{campaign_id}/email-activity` —
     per-subscriber event stream. **Very large**: always page with
     `count` (max 1000) + `offset`, and pass `since` to bound the window.
   - `getReportsIdOpenDetails`, `getReportsIdClickDetails`, `getReportsIdSentTo`.

## Rules an agent must follow

- Page every list endpoint on `count`/`offset` and stop at `total_items`. Do not
  assume a single response is complete.
- Use `fields` / `exclude_fields` on every report call — these payloads are the
  main cause of the 120-second timeout.
- Keep concurrency at or below **10** connections; `429` (or a bare `403` at high
  volume) is the throttling signal and there are no `X-RateLimit-*` headers to
  pace against.
- For large or repeated extractions, submit the reads through `POST /batches`
  (`skills/mailchimp-bulk-sync-with-batches.md`) instead of looping live calls.
- These are opens/clicks on real people. Apple Mail Privacy Protection inflates
  open counts — do not present `open_rate` as ground truth in any downstream
  decision an agent makes on its own.
