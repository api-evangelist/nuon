---
name: Subscribe to org workflow lifecycle webhooks
description: Register, scope, rotate, and remove org-scoped webhooks that deliver Nuon workflow lifecycle events as signed CloudEvents.
api: openapi/nuon-oapi-v3-openapi.json
operations: [CreateCurrentOrgWebhook, GetCurrentOrgWebhooks, UpdateCurrentOrgWebhook, DeleteCurrentOrgWebhook]
---

# Subscribe to org workflow lifecycle webhooks

Org webhooks POST CloudEvents v1.0 envelopes to your HTTPS endpoint whenever a workflow or workflow step transitions. See asyncapi/nuon-webhooks-asyncapi.yml for the event schema.

## Steps
1. **List webhooks** — call `GetCurrentOrgWebhooks` to see current subscriptions (each shows `has_secret: true|false`; the secret is never returned).
2. **Create a webhook** — call `CreateCurrentOrgWebhook` with an absolute `https` `url`, an optional `secret`, and an optional subscription (`interests` + `match`). Omitting `interests` defaults to `{ "all_events": true }`.
3. **Scope it** — narrow with `interests.resources` (per-resource `ops`/`outcome`/`approval_requests`/`approval_responses`/`drift_detected`) and/or a `match` predicate (`installs`/`components`/`actions` ids or a label `selector`).
4. **Rotate/retarget** — call `UpdateCurrentOrgWebhook`; it replaces `interests` and `match` wholesale (not a merge). Pass a new `secret` to rotate signing; the URL cannot be changed in place.
5. **Delete** — call `DeleteCurrentOrgWebhook` with the webhook id.

## Rules
- Verify every delivery: reject any request whose `X-Nuon-Signature` (lowercase hex HMAC-SHA256 of the raw body, keyed by your secret) does not match.
- Make handlers **idempotent** — derive an idempotency key from workflow/step/resource/transition fields, since duplicate deliveries may arrive with different CloudEvents `id`s.
- Ack with `2xx` within 5 seconds; there are no retries or replay. `(org_id, webhook_url, match)` is the uniqueness key — registering the same pair twice returns `409`.
