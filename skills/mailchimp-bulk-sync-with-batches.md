---
name: Bulk-sync contacts with the Mailchimp Batch endpoint
description: Run up to 1,000 Marketing API operations asynchronously in one request instead of looping, then poll the batch to completion and read the result file.
api: openapi/mailchimp-batches-api-openapi.yml
generated: '2026-08-13'
method: generated
source: >-
  Grounded in operationIds verified in openapi/mailchimp-marketing-api-openapi-original.json
  (Mailchimp Marketing API 3.0.91, harvested 2026-08-13) plus
  https://mailchimp.com/developer/marketing/guides/run-async-requests-batch-endpoint/
  and https://mailchimp.com/developer/marketing/docs/fundamentals/ (API limits).
operations:
  - postBatches
  - getBatchesId
  - getBatches
  - deleteBatchesId
---

# Bulk-sync with the Batch endpoint

The Marketing API allows **10 simultaneous connections** and no more. Any sync
larger than a few dozen records must go through `/batches`, not a request loop —
this is the documented way to avoid the request limits.

## Steps

1. Build the operations array. Each entry is a request the API would have taken
   on its own:
   ```json
   {
     "operations": [
       {
         "method": "PUT",
         "path": "/lists/{list_id}/members/{subscriber_hash}",
         "operation_id": "your-own-correlation-id",
         "body": "{\"email_address\":\"…\",\"status_if_new\":\"subscribed\"}"
       }
     ]
   }
   ```
   - `body` is a **JSON string**, not a nested object.
   - `operation_id` is yours; it is echoed back in the results file and is how you
     reconcile outcomes. Set it to a stable key (e.g. your record id) so a rerun
     is reconcilable.
   - Ceiling: **1,000 operations per request**, **500 open batches per account**.
2. `postBatches` — `POST /batches` — submit. Keep the returned batch `id`.
   Record it before doing anything else: without it you must scan `getBatches`
   to find your submission.
3. `getBatchesId` — `GET /batches/{batch_id}` — poll. Read `status`
   (`pending` → `preprocessing` → `started` → `finalizing` → `finished`),
   `total_operations`, `finished_operations`, `errored_operations`.
   Poll no more often than every few seconds; batches are asynchronous by design.
4. When `status` is `finished`, download `response_body_url` — a **gzipped tar of
   JSON files** containing one entry per operation with `status_code`, `response`,
   and your `operation_id`. It is a short-lived link; fetch it promptly.
5. Reconcile: any entry whose `status_code` is not 2xx is a real failure. Re-submit
   only those operations in a new batch.
6. `deleteBatchesId` — `DELETE /batches/{batch_id}` — stop a running batch if you
   submitted the wrong payload. It cannot un-send work already applied.

## Rules an agent must follow

- Batches are **not transactional**. Partial success is the normal outcome; always
  read the results file rather than trusting `status: finished`.
- Prefer `PUT /lists/{list_id}/members/{subscriber_hash}` inside a batch over
  `POST /lists/{list_id}/members` — the `PUT` form is re-runnable, so a whole
  batch can be safely resubmitted.
- Do not submit a second batch for the same records while the first is unfinished;
  there is no idempotency key to deduplicate them.
- The 120-second request timeout applies to the batch *submission*, not to the
  batch's execution.
