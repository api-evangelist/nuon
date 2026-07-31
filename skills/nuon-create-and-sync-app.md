---
name: Create a BYOC app and manage its config
description: Create a Nuon app in the control plane, read and update it, and list existing apps for the org.
api: openapi/nuon-oapi-v3-openapi.json
operations: [CreateApp, GetApps, GetApp, UpdateApp, DeleteApp]
---

# Create a BYOC app and manage its config

A Nuon **app** packages your application (Terraform, Helm, Kubernetes manifests, container images) into an installable BYOC version that deploys into a customer's cloud account.

## Prerequisites
- A valid Bearer token and `X-Nuon-Org-ID` (see nuon-provision-static-token skill).

## Steps
1. **List apps** — call `GetApps` to see the org's existing apps and avoid duplicates.
2. **Create the app** — call `CreateApp` with a name. Names are unique within an org (a duplicate returns `409`).
3. **Read it back** — call `GetApp` with the returned app id to confirm creation and read its config state.
4. **Update** — call `UpdateApp` to change the app's configuration.
5. **Delete** — call `DeleteApp` when decommissioning (this cannot be undone; ensure no active installs remain).

## Rules
- The CLI equivalent `nuon apps sync` pushes the local TOML config directory; the API operates on the same app objects.
- Ids are opaque, prefixed strings. Errors follow the `{ "error": "<message>" }` envelope (see errors/nuon-problem-types.yml).
- See conventions/nuon-conventions.yml for pagination and versioning details.
