---
name: Add and build app components
description: Attach components (Helm, Terraform, container image, Kubernetes manifest) to a Nuon app and build them.
api: openapi/nuon-oapi-v3-openapi.json
operations: [CreateComponent, GetAppComponents, CreateAppComponentBuild, GetAppComponentLatestBuild, UpdateAppComponent]
---

# Add and build app components

**Components** connect your existing artifacts — container images, Helm charts, Kubernetes manifests, Terraform/Pulumi code — into a Nuon app, modeled as a dependency graph.

## Steps
1. **List components** — call `GetAppComponents` for the app.
2. **Create a component** — call `CreateComponent` with the app id and the component type/config.
3. **Build it** — call `CreateAppComponentBuild` to produce a build artifact for the component.
4. **Check the build** — call `GetAppComponentLatestBuild` to read status; a build can be `succeeded`, `failed`, or in progress.
5. **Update** — call `UpdateAppComponent` to change the component's configuration.

## Rules
- Component config is type-specific (docker-build, helm, external-image, kubernetes-manifest, job, pulumi, terraform). Use the matching create-config operations from the `components` tag when authoring config directly.
- Builds and deploys are separate: building produces an artifact; deploying happens per-install (see the install skill).
- Errors use the `{ "error": "<message>" }` envelope; a `409` typically means a duplicate component name.
