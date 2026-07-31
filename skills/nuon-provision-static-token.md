---
name: Create an API token and identify the current account
description: Authenticate against the Nuon control-plane API, confirm the current account/org, and mint or revoke a durable API token.
api: openapi/nuon-oapi-v3-openapi.json
operations: [GetCurrentAccount, CreateStaticToken, ListStaticTokens, DeleteStaticToken]
---

# Create an API token and identify the current account

Use this skill to bootstrap programmatic access to Nuon.

## Auth model
- Send `Authorization: Bearer <api-token>` on every request.
- Send `X-Nuon-Org-ID: <org_id>` to scope requests to a specific org.
- Interactive tokens come from `nuon auth login`; durable tokens are created with `CreateStaticToken` (or `nuon orgs api-tokens create`). Roles: `org_admin`, `org_support`, `org_read_only`.

## Steps
1. **Confirm identity** — call `GetCurrentAccount` to verify the token resolves to an account and to read its orgs.
2. **List existing tokens** — call `ListStaticTokens` to see what is already provisioned before adding another.
3. **Mint a token** — call `CreateStaticToken` with a descriptive name and role. The secret is shown once; store it in a secret manager immediately.
4. **Revoke** — call `DeleteStaticToken` with the token id to rotate or offboard.

## Rules
- Never log or echo the token value; it is returned only on creation.
- Prefer least privilege: `org_read_only` for read integrations.
- A `401` means a missing/expired token; `403` means the token's role or `X-Nuon-Org-ID` does not permit the operation (see errors/nuon-problem-types.yml).
