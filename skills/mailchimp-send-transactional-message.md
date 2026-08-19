---
name: Send a Mailchimp Transactional (Mandrill) message
description: Send a one-to-one transactional email or template send through the Mandrill RPC API, then look the message up by id to confirm delivery state.
api: openapi/mailchimp-messages-api-openapi.yml
generated: '2026-08-13'
method: generated
source: >-
  Grounded in operationIds verified in openapi/mailchimp-transactional-api-openapi-original.json
  (Mailchimp Transactional API 1.4.1, harvested 2026-08-13 from
  github.com/mailchimp/mailchimp-client-lib-codegen) plus
  https://mailchimp.com/developer/transactional/docs/fundamentals/ and
  sandbox/mailchimp-sandbox.yml.
operations:
  - postUsersPing
  - postMessagesSend
  - postMessagesSendTemplate
  - postMessagesInfo
  - postMessagesSearch
  - postMessagesCancelScheduled
---

# Send a Transactional (Mandrill) message

Transactional is **not** REST. Every call is an HTTP `POST` with a JSON body, the
API key travels **in the body** as `key`, and any non-`200` status is an error.

- Root: `https://mandrillapp.com/api/1.0/` (the published docs root). The
  first-party spec declares `basePath: /api/1.3`; both are live — pin the one your
  client library uses and do not mix them mid-flow.
- Path form: `/{group}/{method}.{format}` — e.g.
  `https://mandrillapp.com/api/1.0/messages/send.json`. Output formats: `json`
  (default), `xml`, `yaml`, `php`.

## Steps

1. `postUsersPing` — `POST /users/ping` — cheapest credential check. A valid key
   returns `"PONG!"`; a bad one returns `401 Invalid_Key`.
2. `postMessagesSend` — `POST /messages/send`:
   ```json
   {
     "key": "<API key>",
     "message": {
       "from_email": "…",
       "subject": "…",
       "html": "…",
       "to": [{ "email": "…", "type": "to" }]
     }
   }
   ```
   Or `postMessagesSendTemplate` — `POST /messages/send-template` — with
   `template_name` + `template_content` + `merge_vars`.
3. The response is an **array with one entry per recipient**:
   `{ "email", "status", "reject_reason", "_id" }`. `status` is `sent`, `queued`,
   `scheduled`, `rejected`, or `invalid`. **A `200` does not mean delivered** —
   read `status` per recipient and treat `rejected`/`invalid` as failures, using
   `reject_reason` (`hard-bounce`, `soft-bounce`, `spam`, `unsub`, `rule`, …).
4. Keep `_id` per recipient. `postMessagesInfo` — `POST /messages/info` with
   `{"id": "<_id>"}` — returns the delivery state, opens, and clicks.
   `postMessagesSearch` searches recent activity when you lost the id.
5. Scheduled sends (`send_at`, requires a paid account) can be listed with
   `postMessagesListScheduled` and stopped with `postMessagesCancelScheduled`.

## Rules an agent must follow

- **No idempotency key exists.** A retry after a timeout sends a second email.
  Before retrying, call `postMessagesSearch` (or `postMessagesInfo` if you have
  the `_id`) and confirm the first attempt did not land.
- **Test safely.** Create a **test API key** in the Mandrill UI
  (Settings → + New API Key → check *Test Key*). Test-mode sends deliver nothing,
  do not count toward send totals, and do not affect reputation — 10,000/day limit
  (`sandbox/mailchimp-sandbox.yml`). Use it for every dry run.
- Transactional stores no contact lists. Your database is the source of truth for
  addresses; Mailchimp only sees what you pass in the request.
- Sending domains must have DKIM/DMARC configured and verified
  (`postSendersCheckDomain`) or delivery quality collapses.
- Outbound events (send, bounce, open, click) arrive via the separate
  Transactional webhook surface (`postWebhooksAdd`), not the Marketing webhooks.
