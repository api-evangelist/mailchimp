---
name: Upsert a Mailchimp audience member and tag them
description: Add or update a contact in a Mailchimp audience (list) idempotently by email hash, then apply tags — the safest write path for an agent syncing contacts.
api: openapi/mailchimp-lists-api-openapi.yml
generated: '2026-08-13'
method: generated
source: >-
  Grounded in operationIds verified in openapi/mailchimp-marketing-api-openapi-original.json
  (Mailchimp Marketing API 3.0.91, harvested 2026-08-13) plus
  https://mailchimp.com/developer/marketing/docs/fundamentals/ and
  conventions/mailchimp-conventions.yml.
operations:
  - getRoot
  - getLists
  - putListsIdMembersId
  - getListsIdMembersId
  - postListMemberTags
---

# Upsert a Mailchimp audience member

Use this when a contact must exist in a Mailchimp audience with known field values.
`PUT` is the only member write that is safe to retry — Mailchimp has **no**
`Idempotency-Key` header (see `conventions/mailchimp-conventions.yml`), so
idempotence comes from addressing the resource by its subscriber hash.

## Before you call

1. **Resolve the data center.** The base URL is `https://<dc>.api.mailchimp.com/3.0`.
   `<dc>` is the suffix of the API key after the dash (`…-us19` → `us19`), or the
   `dc` field returned by the OAuth metadata endpoint. Calling the wrong `<dc>`
   returns an error, not a redirect.
2. **Authenticate.** HTTP Basic with any username and the API key as the password,
   or `Authorization: Bearer <token>` with an OAuth 2 access token. Mailchimp OAuth
   grants full account access — there are no granular scopes
   (`authentication/mailchimp-authentication.yml`).
3. **Confirm the credential and role** with `getRoot` (`GET /`). It returns the
   account plus the role of the authorizing user. Actions outside that role return
   `403`.

## Steps

1. `getLists` — `GET /lists` — find the target audience `id`. Paginate with
   `count` (max 1000) and `offset`; read `total_items` to know when to stop.
   Use `fields=lists.id,lists.name,total_items` to keep the payload small.
2. Compute the **subscriber hash**: lowercase the email address, then MD5 it.
   This is the member id in every member path.
3. `putListsIdMembersId` — `PUT /lists/{list_id}/members/{subscriber_hash}` —
   send `email_address`, `status_if_new` (`subscribed` | `pending`), and
   `merge_fields`. This creates the member when absent and updates them when
   present, so a retry after a timeout is safe.
   - Use `status_if_new: pending` when you do not have provable consent — it
     triggers the double opt-in email instead of subscribing silently.
   - Never use `postListsIdMembers` (`POST /lists/{list_id}/members`) in an agent
     loop: a retry on an already-created member returns `400 Member Exists`.
4. `postListMemberTags` — `POST /lists/{list_id}/members/{subscriber_hash}/tags` —
   apply tags as `{"tags":[{"name":"vip","status":"active"}]}`. `status: inactive`
   removes a tag. The call is a set operation and is safe to repeat.
5. `getListsIdMembersId` — `GET /lists/{list_id}/members/{subscriber_hash}` —
   read back to confirm `status`, `tags`, and `merge_fields`.

## Rules an agent must follow

- **Throttling:** 10 simultaneous connections per user. Exceeding it returns `429`,
  and at very high volume a `403` with no JSON body. There are no `X-RateLimit-*`
  response headers to read — hold your own concurrency to ≤ 10 and back off on
  `429`/`403` (`rate-limits/mailchimp-rate-limits.yml`).
- **Timeout:** requests are cut at 120 seconds.
- **Errors** are `application/problem+json` (`type`, `title`, `status`, `detail`,
  `instance`); branch on `status` + `title`, never on `detail` prose
  (`errors/mailchimp-problem-types.yml`).
- **More than a handful of contacts?** Do not loop — use the batch flow in
  `skills/mailchimp-bulk-sync-with-batches.md`.
- **Compliance:** do not re-subscribe an address whose status is `unsubscribed` or
  `cleaned`. Mailchimp rejects it, and doing it deliberately is a consent violation.
