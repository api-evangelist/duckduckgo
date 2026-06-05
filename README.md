# DuckDuckGo (duckduckgo)

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
