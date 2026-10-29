# DuckDuckGo

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

DuckDuckGo is an independent online-privacy company best known for its tracker-free search engine and the DuckDuckGo Browser (iOS, Android, macOS, Windows). It operates the public Instant Answer API at api.duckduckgo.com (free, JSON/XML), the Duck.ai anonymous AI-chat proxy at duck.ai (routes to Anthropic Claude, OpenAI GPT, Meta Llama, Mistral models without storing or training on prompts), the Tracker Radar open dataset (CC BY-NC-SA), Email Protection (@duck.com forwarding addresses), and Privacy Pro (VPN + Personal Information Removal + Identity Theft Restoration).

**Areas:** Search · Privacy · Browser · AI Chat · Email Protection · VPN · Trackers · Identity

## DuckDuckGo on APIs.io

Everything profiled for DuckDuckGo is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/duckduckgo/](https://apis.io/providers/duckduckgo/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Duck.ai Anonymous AI Chat](https://apis.io/apis/duckduckgo/duck-ai/) — Duck.ai is DuckDuckGo's anonymizing proxy in front of third-party LLMs. Free tier currently includes Anthropic Claude 4.5 Haiku, Meta Llama 4 Scout, Mistral…
- [DuckDuckGo Tracker Radar Dataset](https://apis.io/apis/duckduckgo/tracker-radar/) — Tracker Radar is the open dataset that powers DuckDuckGo's tracker and fingerprinting protection. It is a JSON corpus of the most common third-party domains…
- [DuckDuckGo !Bang Redirector](https://apis.io/apis/duckduckgo/bang-redirector/) — The !bang system - in place since 2008 and now spanning thousands of destinations - lets a query like "!w filter bubble" 302-redirect to the destination…
- [DuckDuckGo Instant Answers API](https://apis.io/apis/duckduckgo/duckduckgo-instant-answers-api/) — Zero-click answers, abstracts, definitions and disambiguations.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### JSON Schema (2)

The data models the API reads and writes.

- [DuckDuckGo Instant Answer Response](https://apis.io/schemas/duckduckgo/instant-answer-response/)
- [DuckDuckGo Tracker Radar Domain Record](https://apis.io/schemas/duckduckgo/tracker-radar-domain/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Instant Answer Response Structure](https://apis.io/json-structure/duckduckgo/instant-answer-response-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Duckduckgo Context](https://apis.io/jsonld/duckduckgo/duckduckgo-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Duckduckgo Vocabulary](https://apis.io/vocabularies/duckduckgo/duckduckgo-vocabulary/)

#### Examples (4)

Example requests and responses.

- [Instant Answer Bang Example](https://apis.io/examples/duckduckgo/instant-answer-bang-example/)
- [Instant Answer Calc Example](https://apis.io/examples/duckduckgo/instant-answer-calc-example/)
- [Instant Answer Topic Example](https://apis.io/examples/duckduckgo/instant-answer-topic-example/)
- [Tracker Radar Domain Example](https://apis.io/examples/duckduckgo/tracker-radar-domain-example/)

#### Collections (2)

Postman and Open Collection request collections.

- [DuckDuckGo Instant Answer Bangs API](https://apis.io/collections/duckduckgo/open-duckduckgo-bangs-api/)
- [DuckDuckGo Instant Answer Instant Answers API](https://apis.io/collections/duckduckgo/open-duckduckgo-instant-answers-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [DuckDuckGo — jsonschema rules](https://apis.io/rules/duckduckgo/duckduckgo-jsonschema-spectral-rules/)
- [DuckDuckGo — instant answer rules](https://apis.io/rules/duckduckgo/instant-answer-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Duckduckgo Domain Security](https://apis.io/security/duckduckgo/duckduckgo-domain-security/)
- [Duckduckgo Vulnerability Disclosure](https://apis.io/security/duckduckgo/duckduckgo-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Duckduckgo Plans Pricing](https://apis.io/plans/duckduckgo/duckduckgo-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Duckduckgo Rate Limits](https://apis.io/rate-limits/duckduckgo/duckduckgo-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Duckduckgo Finops](https://apis.io/finops/duckduckgo/duckduckgo-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://duckduckgo.com/)
- [Blog](https://spreadprivacy.com/)
- [Privacy policy](https://duckduckgo.com/privacy)
- [GitHub](https://github.com/duckduckgo)

## API Evangelist rating

**Kin Score 38.5** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 57.8 |
| Contract governance | 27.3 |
| Operational transparency | 26.3 |
| Developer ergonomics | 21.4 |
| Access clarity | 28.9 |

**Agent readiness 21.6** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | na |
| Error Semantics | — |
| OpenAPI Examples | verified |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 20.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/duckduckgo/](https://apis.io/providers/duckduckgo/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for DuckDuckGo: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/duckduckgo/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
