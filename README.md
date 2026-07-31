# Nuon

Nuon is a Bring Your Own Cloud (BYOC) continuous-delivery platform for software vendors. It lets vendors package existing applications — Terraform, Pulumi, Helm charts, Kubernetes manifests, and container images — and deploy them into their customers' own AWS, Azure, or GCP accounts while keeping a SaaS-like experience.

Nuon runs a Control Plane plus egress-only Runners inside each customer account (no cross-account IAM), with day-2 operations: least-privilege operation roles, drift detection, approval workflows, OPA policies, runbooks, secrets, actions, and org-scoped CloudEvents webhooks. It exposes a REST control-plane API (OpenAPI v2 + v3), a first-party CLI/TUIs, Go/Python/Elixir SDKs, and Terraform providers. Core is open source at https://github.com/nuonco.

- Website: https://nuon.co/
- Docs: https://docs.nuon.co
- API reference: https://docs.nuon.co/nuon-api
- OpenAPI: https://api.nuon.co/oapi/v3 (v3), https://api.nuon.co/oapi/v2 (v2)
- Status: https://status.nuon.co
- Trust: https://trust.nuon.co

Backed by: redpoint-ventures, uncork-capital
