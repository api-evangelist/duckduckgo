# DuckDuckGo

DuckDuckGo is an independent online-privacy company best known for its tracker-free search engine and the DuckDuckGo Browser (iOS, Android, macOS, Windows). It also operates the **public Instant Answer API** at `api.duckduckgo.com`, the **Duck.ai** anonymous AI-chat proxy at `duck.ai`, the **Tracker Radar** open dataset, **Email Protection** (@duck.com forwarding addresses), and **Privacy Pro** (VPN + Personal Information Removal + Identity Theft Restoration).

> "Independent online protection company. Get our mobile & desktop browser with protections built-in, including our search engine that doesn't track you." — DuckDuckGo GitHub org description

This repository is an [API Evangelist](https://apievangelist.com) profile of DuckDuckGo's developer-facing surface. It is generated from public documentation, the GitHub org, and live calls against `api.duckduckgo.com`.

## APIs profiled

| API | Surface | Status |
| --- | --- | --- |
| **DuckDuckGo Instant Answer API** | `https://api.duckduckgo.com` (free, key-less, JSON/XML/JSON-P) | Public, documented |
| **Duck.ai** | `https://duck.ai` (web UI; anonymous proxy to Claude, GPT, Llama, Mistral, gpt-oss) | Public, no REST API |
| **Tracker Radar dataset** | `https://github.com/duckduckgo/tracker-radar` (JSON under `/domains`, CC BY-NC-SA 4.0) | Public data API |
| **!Bang Redirector** | `https://duckduckgo.com/bangs` (thousands of registered shortcuts since 2008) | Public |

## Repository contents

- [`apis.yml`](apis.yml) — APIs.json 0.19 master index of all DuckDuckGo APIs and properties.
- [`openapi/instant-answer-openapi.yml`](openapi/instant-answer-openapi.yml) — OpenAPI 3.0.3 description of the Instant Answer API.
- [`examples/`](examples/) — Live-shape request/response examples:
  - `instant-answer-topic-example.json` (topic abstract)
  - `instant-answer-bang-example.json` (!bang redirect with `no_redirect=1`)
  - `instant-answer-calc-example.json` (`AnswerType: calc`)
  - `tracker-radar-domain-example.json` (one Tracker Radar domain entry)
- [`json-schema/`](json-schema/) — JSON Schemas for the Instant Answer envelope and Tracker Radar domain record.
- [`json-structure/`](json-structure/) — JSON Structure description of the Instant Answer response.
- [`json-ld/duckduckgo-context.jsonld`](json-ld/duckduckgo-context.jsonld) — JSON-LD context mapping DuckDuckGo fields onto schema.org.
- [`rules/instant-answer-rules.yml`](rules/instant-answer-rules.yml) — Spectral ruleset enforcing DuckDuckGo conventions (HTTPS api.duckduckgo.com server, required `q`, format enum, etc.).
- [`capabilities/`](capabilities/) — Naftiko capabilities:
  - `shared/instant-answer-capabilities.yaml`
  - `shared/duck-ai-capabilities.yaml`
  - `instant-answer-search-workflow.yaml`
- [`vocabulary/duckduckgo-vocabulary.yml`](vocabulary/duckduckgo-vocabulary.yml) — Domain vocabulary (Bang, Disambiguation, Tracker Radar, Duck.ai, Prevalence, Fingerprinting, …).
- [`plans/duckduckgo-plans-pricing.yml`](plans/duckduckgo-plans-pricing.yml) — API Commons Plans 0.1 capturing free API + Duck.ai Free/Plus/Pro + Privacy Pro + Email Protection.
- [`rate-limits/duckduckgo-rate-limits.yml`](rate-limits/duckduckgo-rate-limits.yml) — Rate-limit posture (Instant Answer API publishes no numeric limits; Tracker Radar inherits GitHub raw-content limits).
- [`finops/duckduckgo-finops.yml`](finops/duckduckgo-finops.yml) — FinOps profile (developer surface is free; commercial surface is consumer SaaS).

## Notable findings

- The **Instant Answer API is real and free, but narrow** — it returns the zero-click "answer box," not the search-results listing. Topical abstracts come primarily from Wikipedia; bang queries return a `Redirect` URL when `no_redirect=1`; direct answers (calculator, color codes, IPs) surface via `Answer` + `AnswerType`.
- **Duck.ai has no developer API**. The free tier exposes Claude 4.5 Haiku, GPT-4o mini, GPT-5 mini, gpt-oss-120b, Llama 4 Scout, and Mistral Small 3 24B; Plus adds Claude Sonnet 4.5, GPT-4o, GPT-5.2, Llama 4 Maverick; Pro adds Claude Opus 4.6 with 2x usage limits. DuckDuckGo positions Duck.ai as "Duck.ai is a feature that allows you to have private conversations with 3rd-party AI chat models, anonymized by us."
- **Tracker Radar is a credible data API** (raw JSON in GitHub, CC BY-NC-SA 4.0, used by other privacy tooling). Treat the repo as the API surface and the per-domain JSON files as records.
- DuckDuckGo's **GitHub org carries ~123 repos** dominated by browser implementations (Android, apple-browsers, the now-archived help-pages site, the privacy extension), tracker / autoconsent / content-scope-scripts tooling, and the privacy-configuration library.

## Notable absences

- **No public OpenAPI** is published by DuckDuckGo for the Instant Answer API; the spec in this repo is derived from the documentation page and from live calls.
- **No documented numeric rate limits** for the Instant Answer API.
- **No developer API for Duck.ai** — only the consumer UI / browser integration.
- **No public pricing API or billing webhooks** for Duck.ai Plus/Pro or Privacy Pro.

## Maintainer

- Kin Lane — <kin@apievangelist.com>
