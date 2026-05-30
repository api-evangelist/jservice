# jService (jservice)

jService is an open source Ruby on Rails trivia API that serves approximately 200,000 Jeopardy! questions, answers, and categories sourced from the [J! Archive](https://j-archive.com) fan site.

**APIs.yml:** [apis.yml](apis.yml)

## Status

- **x-type:** opensource
- **x-status:** **deprecated** — the historical hosted endpoint at `http://jservice.io` is offline (parked / for-sale holding page).
- **x-tier:** 3 (bulk-registered from public-apis)
- **x-license:** MIT
- **x-language:** Ruby (Rails 7, PostgreSQL)
- **x-governance:** community (single-maintainer)
- **Source repo:** [sottenad/jService](https://github.com/sottenad/jService) — last pushed 2024-01-30, 486 stars, 91 forks, not archived.
- **Original catalog source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Games & Comics.

Although the public endpoint is gone, the project is still self-hostable. The OpenAPI spec in this repo is reconstructed from the upstream source so the historical API surface is preserved.

## API

- **jService Trivia API** — [Source](https://github.com/sottenad/jService) · [OpenAPI](openapi/jservice-openapi.yml)

### Endpoints

| Method | Path | Description |
|---|---|---|
| GET | `/api/random` | Get N random clues (max 100) with parent category. |
| GET | `/api/final` | Get N random Final Jeopardy clues (clues with no value). |
| GET | `/api/clues` | List clues filtered by value, category, airdate, game ID; paginated. |
| GET | `/api/categories` | List categories with offset/count pagination. |
| GET | `/api/category` | Get a single category by `id`, including its clues. |
| POST | `/api/invalid` | Flag a clue as invalid (increments `invalid_count`). |

No authentication. No documented rate limits.

## Artifacts

### OpenAPI
- [openapi/jservice-openapi.yml](openapi/jservice-openapi.yml)

### JSON Schema
- [json-schema/jservice-clue-schema.json](json-schema/jservice-clue-schema.json)
- [json-schema/jservice-category-schema.json](json-schema/jservice-category-schema.json)

### JSON Structure
- [json-structure/jservice-clue-structure.json](json-structure/jservice-clue-structure.json)
- [json-structure/jservice-category-structure.json](json-structure/jservice-category-structure.json)

### JSON-LD
- [json-ld/jservice-context.jsonld](json-ld/jservice-context.jsonld)

### Examples
- [examples/jservice-random-example.json](examples/jservice-random-example.json)
- [examples/jservice-final-example.json](examples/jservice-final-example.json)
- [examples/jservice-clues-example.json](examples/jservice-clues-example.json)
- [examples/jservice-categories-example.json](examples/jservice-categories-example.json)
- [examples/jservice-category-example.json](examples/jservice-category-example.json)
- [examples/jservice-invalid-example.json](examples/jservice-invalid-example.json)

### Spectral Rules
- [rules/jservice-rules.yml](rules/jservice-rules.yml)

### Vocabulary
- [vocabulary/jservice-vocabulary.yml](vocabulary/jservice-vocabulary.yml)

## Naftiko Capabilities

Capabilities are split per OpenAPI tag, each self-contained (consumes + REST exposer + MCP exposer).

### jService Trivia API
- [capabilities/jservice-clues.yaml](capabilities/jservice-clues.yaml) — 3 operations (random, final, list)
- [capabilities/jservice-categories.yaml](capabilities/jservice-categories.yaml) — 2 operations (list, get)
- [capabilities/jservice-moderation.yaml](capabilities/jservice-moderation.yaml) — 1 operation (mark invalid)

## Tags

Games And Comics, Trivia, Jeopardy, Open Source, Ruby, Rails, Public APIs

## Notes

- This entry was bulk-registered as part of a public-apis catalog sweep on 2026-05-28 and enriched on 2026-05-30.
- The hosted endpoint at jservice.io is offline. To use the API, clone [sottenad/jService](https://github.com/sottenad/jService), run against PostgreSQL, and populate via `rake 'get_clues[1,38]'`.
- Tooling note: no MCP server or Claude Code skills published by upstream; no Kubernetes CRDs; no commercial plans, rate limits, or FinOps artifacts.

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## Maintainers

- **Kin Lane** — kin@apievangelist.com
