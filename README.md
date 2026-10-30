# Nuon

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Nuon is a Bring Your Own Cloud (BYOC) continuous-delivery platform for software vendors. It lets vendors package existing applications — Terraform, Pulumi, Helm charts, Kubernetes manifests, and container images — and deploy them into their customers' own AWS, Azure, or GCP accounts while keeping a SaaS-like experience. Nuon runs a Control Plane plus egress-only Runners installed in each customer account (no cross-account IAM), and adds day-2 operations: least-privilege operation roles, drift detection, approval workflows, OPA-based policies, runbooks, secrets, actions, and org-scoped CloudEvents webhooks. The platform exposes a REST control-plane API (OpenAPI v2 + v3), a first-party CLI and TUIs, Go/Python/Elixir SDKs, and Terraform providers. Nuon's core is open source under github.com/nuonco.

**Areas:** Company · BYOC · Deployment · Continuous Delivery · DevOps · Infrastructure · Cloud · Multi-Cloud · Kubernetes · Terraform · Platform Engineering

## Nuon on APIs.io

Everything profiled for Nuon is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/nuon/](https://apis.io/providers/nuon/)** — or go straight to one of the APIs or properties below.

### APIs (18)

- [Nuon Accounts API](https://apis.io/apis/nuon/nuon-accounts-api/) — accounts
- [Nuon Actions API](https://apis.io/apis/nuon/nuon-actions-api/) — actions
- [Nuon Actions/runner API](https://apis.io/apis/nuon/nuon-actions-runner-api/) — actions/runner
- [Nuon Apps API](https://apis.io/apis/nuon/nuon-apps-api/) — apps
- [Nuon Auth API](https://apis.io/apis/nuon/nuon-auth-api/) — auth
- [Nuon Components API](https://apis.io/apis/nuon/nuon-components-api/) — components
- [Nuon General API](https://apis.io/apis/nuon/nuon-general-api/) — general
- [Nuon Installs API](https://apis.io/apis/nuon/nuon-installs-api/) — installs
- [Nuon Notebooks API](https://apis.io/apis/nuon/nuon-notebooks-api/) — notebooks
- [Nuon Onboarding API](https://apis.io/apis/nuon/nuon-onboarding-api/) — onboarding
- [Nuon Orgs API](https://apis.io/apis/nuon/nuon-orgs-api/) — orgs
- [Nuon Policy Reports API](https://apis.io/apis/nuon/nuon-policy-reports-api/) — policy-reports
- [Nuon Queues API](https://apis.io/apis/nuon/nuon-queues-api/) — queues
- [Nuon Runbooks API](https://apis.io/apis/nuon/nuon-runbooks-api/) — runbooks
- [Nuon Runners API](https://apis.io/apis/nuon/nuon-runners-api/) — runners
- [Nuon Runners/runner API](https://apis.io/apis/nuon/nuon-runners-runner-api/) — runners/runner
- [Nuon Slack API](https://apis.io/apis/nuon/nuon-slack-api/) — slack
- [Nuon VCS API](https://apis.io/apis/nuon/nuon-vcs-api/) — vcs

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Nuon Org Webhooks](https://apis.io/asyncapis/nuon/nuon-webhooks-asyncapi/)

#### Event channels (2)

Individual events and webhooks the provider emits.

- [com.nuon.workflow.lifecycle.v1](https://apis.io/channels/nuon/com-nuon-workflow-lifecycle-v1/)
- [com.nuon.workflow_step.lifecycle.v1](https://apis.io/channels/nuon/com-nuon-workflow-step-lifecycle-v1/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [nuon](https://apis.io/servers/nuon/nuon/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Nuon Agentic Access](https://apis.io/agentic-access/nuon/nuon-agentic-access/)

#### Collections (18)

Postman and Open Collection request collections.

- [Nuon accounts API](https://apis.io/collections/nuon/open-nuon-accounts-api/)
- [Nuon accounts actions API](https://apis.io/collections/nuon/open-nuon-actions-api/)
- [Nuon accounts actions/runner API](https://apis.io/collections/nuon/open-nuon-actions-runner-api/)
- [Nuon accounts apps API](https://apis.io/collections/nuon/open-nuon-apps-api/)
- [Nuon accounts auth API](https://apis.io/collections/nuon/open-nuon-auth-api/)
- [Nuon accounts components API](https://apis.io/collections/nuon/open-nuon-components-api/)
- [Nuon accounts general API](https://apis.io/collections/nuon/open-nuon-general-api/)
- [Nuon accounts installs API](https://apis.io/collections/nuon/open-nuon-installs-api/)
- [Nuon accounts notebooks API](https://apis.io/collections/nuon/open-nuon-notebooks-api/)
- [Nuon accounts onboarding API](https://apis.io/collections/nuon/open-nuon-onboarding-api/)
- [Nuon accounts orgs API](https://apis.io/collections/nuon/open-nuon-orgs-api/)
- [Nuon accounts policy-reports API](https://apis.io/collections/nuon/open-nuon-policy-reports-api/)
- [Nuon accounts queues API](https://apis.io/collections/nuon/open-nuon-queues-api/)
- [Nuon accounts runbooks API](https://apis.io/collections/nuon/open-nuon-runbooks-api/)
- [Nuon accounts runners API](https://apis.io/collections/nuon/open-nuon-runners-api/)
- [Nuon accounts runners/runner API](https://apis.io/collections/nuon/open-nuon-runners-runner-api/)
- [Nuon accounts slack API](https://apis.io/collections/nuon/open-nuon-slack-api/)
- [Nuon accounts vcs API](https://apis.io/collections/nuon/open-nuon-vcs-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Nuon Oapi V3 Overlay](https://apis.io/overlays/nuon/nuon-oapi-v3-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Nuon Authentication](https://apis.io/security/nuon/nuon-authentication/)
- [Nuon Domain Security](https://apis.io/security/nuon/nuon-domain-security/)
- [Nuon Trust Center](https://apis.io/security/nuon/nuon-trust-center/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://nuon.co/)
- [Documentation](https://docs.nuon.co)
- [Getting started](https://docs.nuon.co/get-started/introduction)
- [API reference](https://docs.nuon.co/nuon-api)
- [Pricing](https://nuon.co/pricing)
- [Sign up](https://app.nuon.co/api/auth/login)
- [Support](https://docs.nuon.co/support/support)
- [Changelog](https://docs.nuon.co/updates/updates)
- [Blog](https://nuon.co/blog)
- [Compliance](https://trust.nuon.co)
- [Terms of service](https://nuon.co/terms)
- [Privacy policy](https://nuon.co/privacy)
- [GitHub](https://github.com/nuonco)
- [Status](https://status.nuon.co)

## API Evangelist rating

**Kin Score 55.9** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 61.1 |
| Contract governance | 4.5 |
| Operational transparency | 34.2 |
| Developer ergonomics | 73.2 |
| Access clarity | 47.4 |

**Agent readiness 36.2** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | — |

**Regulatory alignment 29.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/nuon/](https://apis.io/providers/nuon/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Nuon: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/nuon/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
