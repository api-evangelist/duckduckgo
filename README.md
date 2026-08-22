# DuckDuckGo (duckduckgo)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/duckduckgo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/duckduckgo/refs/heads/main/apis.yml)

## Tags

- Search
- Privacy
- Browser
- AI Chat
- Email Protection
- VPN
- Trackers
- Identity

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### DuckDuckGo Instant Answer API

The DuckDuckGo Instant Answer API returns the boxed answer that appears above DuckDuckGo search results - topic summaries (largely sourced from Wikipedia / structured sites), definitions, categories, disambiguations, and !bang redirects. It is a free, key-less GET endpoint that returns JSON (default), JSON-P (via callback) or XML. It does not return the DuckDuckGo search-results listing itself; it returns only zero-click / instant-answer payloads (Abstract, Answer, Definition, RelatedTopics, Results, Redirect for bangs, plus Image/Heading/Type metadata). Attribution to DuckDuckGo is required when displayed.

- **Human URL:** [https://duckduckgo.com/api](https://duckduckgo.com/api)
- **Base URL:** `https://api.duckduckgo.com`

#### Tags

- Search
- Instant Answer
- Public API
- Free

#### Properties

- [Documentation](https://duckduckgo.com/api)
- [OpenAPI](openapi/instant-answer-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Examples](examples/)
- [Capabilities](capabilities/shared/instant-answer-capabilities.yaml)
- [Spectral Rules](rules/instant-answer-rules.yml)
- [JSON Schema](json-schema/instant-answer-response-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/duckduckgo-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Pricing](https://duckduckgo.com/api)

### Duck.ai Anonymous AI Chat

Duck.ai is DuckDuckGo's anonymizing proxy in front of third-party LLMs. Free tier currently includes Anthropic Claude 4.5 Haiku, Meta Llama 4 Scout, Mistral Small 3 24B, OpenAI GPT-4o mini / GPT-5 mini / gpt-oss-120b. Duck.ai Plus adds GPT-4o, GPT-5.2, Claude Sonnet 4.5, Llama 4 Maverick. Duck.ai Pro adds Claude Opus 4.6, higher reasoning effort and 2x usage limits. DuckDuckGo strips IP / identifiers before forwarding to upstream model providers and does not retain prompts or train on them. There is no public REST API; access is via the web UI and the in-browser integration in DuckDuckGo Browser.

- **Human URL:** [https://duck.ai/](https://duck.ai/)
- **Base URL:** `https://duck.ai`

#### Tags

- AI Chat
- LLM Proxy
- Privacy
- Anonymous

#### Properties

- [Documentation](https://duckduckgo.com/duckduckgo-help-pages/duckai/)
- [Portal](https://duck.ai/)
- [Pricing](plans/duckduckgo-plans-pricing.yml)
- [Capabilities](capabilities/shared/duck-ai-capabilities.yaml)

### DuckDuckGo Tracker Radar Dataset

Tracker Radar is the open dataset that powers DuckDuckGo's tracker and fingerprinting protection. It is a JSON corpus of the most common third-party domains on the web, with metadata covering behavior, classification, ownership, prevalence, fingerprinting, cookies, privacy policies, and performance. Distributed under Creative Commons BY-NC-SA 4.0 (commercial licensing available on request). Files are addressable as raw JSON under /domains in the GitHub repo, so it is consumable as a static read-only "data API" over HTTPS.

- **Human URL:** [https://github.com/duckduckgo/tracker-radar](https://github.com/duckduckgo/tracker-radar)
- **Base URL:** `https://raw.githubusercontent.com/duckduckgo/tracker-radar/main/`

#### Tags

- Trackers
- Open Data
- Privacy Dataset
- JSON

#### Properties

- [Source Code](https://github.com/duckduckgo/tracker-radar)
- [License](https://creativecommons.org/licenses/by-nc-sa/4.0/)
- [JSON Schema](json-schema/tracker-radar-domain-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Examples](examples/tracker-radar-domain-example.json)

### DuckDuckGo !Bang Redirector

The !bang system - in place since 2008 and now spanning thousands of destinations - lets a query like "!w filter bubble" 302-redirect to the destination site's own search (Wikipedia in that example). When called via the Instant Answer API, a bang query returns a Redirect field with the target URL rather than performing the redirect, so it can be used programmatically as a normalized "search-on-other-site" router.

- **Human URL:** [https://duckduckgo.com/bangs](https://duckduckgo.com/bangs)
- **Base URL:** `https://duckduckgo.com/`

#### Tags

- Search
- Redirect
- Bang

#### Properties

- [Documentation](https://duckduckgo.com/bangs)
- [Submission](https://duckduckgo.com/newbang)

## Common Properties

- [Website](https://duckduckgo.com/)
- [Portal](https://duckduckgo.com/duckduckgo-help-pages/)
- [Blog](https://spreadprivacy.com/)
- [Blog R S S](https://spreadprivacy.com/rss/)
- [GitHub Organization](https://github.com/duckduckgo)
- [Source Code](https://github.com/duckduckgo)
- [Browser](https://duckduckgo.com/app)
- [A I Chat](https://duck.ai/)
- [Email Protection](https://duckduckgo.com/email/)
- [Privacy Pro](https://duckduckgo.com/privacy-pro)
- [Privacy Policy](https://duckduckgo.com/privacy)
- [Plans](plans/duckduckgo-plans-pricing.yml)
- [Rate Limits](rate-limits/duckduckgo-rate-limits.yml)
- [Fin Ops](finops/duckduckgo-finops.yml)
- [Vocabulary](vocabulary/duckduckgo-vocabulary.yml)
- [JSON-LD](json-ld/duckduckgo-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [L L Ms Txt](https://duck.ai/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
