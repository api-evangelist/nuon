---
name: Create an install and follow its provision workflow
description: Create an install of a Nuon app into a customer cloud account and track the provision workflow to completion.
api: openapi/nuon-oapi-v3-openapi.json
operations: [CreateInstall, GetAppInstalls, GetInstall, GetInstallWorkflow, GetInstallWorkflowSteps, DeleteInstall]
---

# Create an install and follow its provision workflow

An **install** is a deployment of an app into one customer's cloud account. Provisioning runs as a **workflow** of ordered **steps** (sandbox runs, component deploys).

## Steps
1. **List installs** — call `GetAppInstalls` for the app to see existing installs.
2. **Create the install** — call `CreateInstall` with the app id and the required inputs. This kicks off a provision workflow.
3. **Read the install** — call `GetInstall` to get the install id, status, and current workflow reference.
4. **Follow the workflow** — call `GetInstallWorkflow` for the provision workflow, then `GetInstallWorkflowSteps` to watch each step transition through `started` → `succeeded` / `failed` / `cancelled`.
5. **Tear down** — call `DeleteInstall` to deprovision when finished.

## Rules
- Prefer webhooks over polling for lifecycle: subscribe to `com.nuon.workflow.lifecycle.v1` / `com.nuon.workflow_step.lifecycle.v1` (see the nuon-subscribe-org-webhooks skill and asyncapi/nuon-webhooks-asyncapi.yml).
- Install ids are prefixed `ins_`; workflow ids `inw`, step ids `iws_`.
- Provisioning touches the customer's cloud via an egress-only runner; a `failed` step surfaces `data.outcome.error`.
