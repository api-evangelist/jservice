# jService (jservice)

jService is an open source Ruby on Rails trivia API that serves approximately 200,000 Jeopardy! questions, answers, and categories scraped from the J! Archive fan site. The original public deployment at jservice.io is no longer operational, but the project (sottenad/jService, MIT licensed) remains available for self-hosting against PostgreSQL. The API exposes random clues, final Jeopardy clues, filtered clue queries, category listings, single-category lookup, and invalid-clue reporting under /api/*.

**APIs.json:** [https://github.com/sottenad/jService](https://github.com/sottenad/jService)

## Tags

- Games And Comics
- Trivia
- Jeopardy
- Open Source
- Ruby
- Rails
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### jService Trivia API

REST/JSON API exposing Jeopardy! clues, categories, and random questions, designed for trivia apps, study tools, chatbots, and game shows. Self-hosted against PostgreSQL; the historical public endpoint at jservice.io is offline.

- **Human URL:** [https://github.com/sottenad/jService](https://github.com/sottenad/jService)
- **Base URL:** `http://jservice.io`

#### Tags

- Trivia
- Jeopardy
- Games And Comics

#### Properties

- [Documentation](https://github.com/sottenad/jService#readme)
- [Source Code](https://github.com/sottenad/jService)
- [OpenAPI](openapi/jservice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/jservice.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jservice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/jservice-clue-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/jservice-category-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/jservice-clue-structure.json)
- [JSON Structure](json-structure/jservice-category-structure.json)
- [JSON-LD](json-ld/jservice-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/jservice-rules.yml)
- [Capabilities](capabilities/trivia-game.yaml)
- [Examples](examples/jservice-random-example.json)
- [Vocabulary](vocabulary/jservice-vocabulary.yml)
- [Status](https://jservice.io)
- [License](https://github.com/sottenad/jService/blob/master/LICENSE.txt)
- [Authentication](undefined)
- [Rate Limit](undefined)

## Common Properties

- [Website](https://github.com/sottenad/jService)
- [Source Code](https://github.com/sottenad/jService)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [License](https://github.com/sottenad/jService/blob/master/LICENSE.txt)
- [Data Source](https://j-archive.com)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
