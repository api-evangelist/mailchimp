---
name: Receive and verify Mailchimp audience webhooks
description: Register an audience webhook, handle the form-urlencoded event envelope, and verify the X-Mailchimp-Signature HMAC before trusting a delivery.
api: openapi/mailchimp-webhooks-api-openapi.yml
generated: '2026-08-13'
method: generated
source: >-
  https://mailchimp.com/developer/marketing/guides/sync-audience-data-webhooks/ (fetched
  2026-08-13, HTTP 200) plus operationIds verified in
  openapi/mailchimp-marketing-api-openapi-original.json (3.0.91). Event contract is
  described in asyncapi/mailchimp-marketing-webhooks-asyncapi.yml.
operations:
  - postListsIdWebhooks
  - getListsIdWebhooks
  - getListsIdWebhooksId
  - deleteListsIdWebhooksId
---

# Receive and verify Mailchimp audience webhooks

Mailchimp pushes audience changes to a callback URL you own. This is the only
near-real-time surface the Marketing API offers — there is no streaming API.

## Register

1. `postListsIdWebhooks` — `POST /lists/{list_id}/webhooks`:
   ```json
   {
     "url": "https://example.com/hooks/mailchimp/<hard-to-guess-secret>",
     "events": { "subscribe": true, "unsubscribe": true, "profile": true,
                 "cleaned": true, "upemail": true, "campaign": true },
     "sources": { "user": true, "admin": true, "api": true }
   }
   ```
   - The create response includes `signing_secret` **once**. Store it immediately;
     it cannot be retrieved later. If lost, delete the webhook and create a new one.
   - `sources.api: true` means your own writes echo back — leave it `false` if you
     do not want to process your own changes.
2. `getListsIdWebhooks` / `getListsIdWebhooksId` — list or read registrations
   before creating another; there is no idempotency key, so a blind retry creates
   a duplicate webhook that will double-deliver.
3. `deleteListsIdWebhooksId` — remove a registration you no longer own.

## Handle a delivery

- Body is `application/x-www-form-urlencoded`, **not** JSON. Envelope:
  `type`, `fired_at`, `data[...]`.
- `type` is one of `subscribe`, `unsubscribe`, `profile`, `cleaned`, `upemail`,
  `campaign`. Branch on `type`.
- **Respond within 10 seconds.** A slow or unavailable endpoint is cancelled and
  retried at increasing intervals over ~75 minutes; persistently failing webhooks
  are dropped or disabled at Mailchimp's discretion. Acknowledge with `200` first,
  process asynchronously.
- Deliveries are at-least-once. Deduplicate on `data[id]` + `type` + `fired_at`.

## Verify the signature (do this before parsing)

When HMAC signing is enabled, every delivery carries:

```
X-Mailchimp-Signature: t=<unix_seconds>,v1=<hex_sha256>
```

1. Parse `t` and `v1` from the header.
2. Reject if `t` is more than **300 seconds** old (replay window).
3. Recompute `HMAC-SHA256(key = signing_secret, message = "{t}.{raw_body}")` over
   the **raw, unmodified request bytes** — do not URL-decode or JSON-parse first.
4. Compare with a constant-time function (`hmac.compare_digest`,
   `crypto.timingSafeEqual`, `hash_equals`). A plain `==` leaks timing.
5. Reject any mismatch with `400`.

## Rules an agent must follow

- Never treat an unverified delivery as an authorization to act. The payload
  carries email addresses; an unsigned POST to a guessable URL is trivially forged.
- The typed event contract lives in
  `asyncapi/mailchimp-marketing-webhooks-asyncapi.yml`; the field set is fully
  documented only for `subscribe` and `unsubscribe`.
- Transactional (Mandrill) webhooks are a **separate** surface with a separate
  registration (`postWebhooksAdd`) and their own signature scheme — do not reuse
  this handler for them.
