# VISEON

**Semantic Intelligence**

*Build Context. Command Visibility.*

[VISEON.IO](https://viseon.io) is a governed data platform for AI discoverability, semantic search and agentic commerce. It turns a website into a complete knowledge graph, an MCP-ready data layer and an agentic commerce catalogue, so AI can **discover**, **discuss** and **transact** with brands, products and services.

This repository is the public face of VISEON.IO. It hosts reference material such as the Schema.org JSON-LD Edge Integrity Test. The platform itself runs at [viseon.io](https://viseon.io).

## Discover, Discuss, Transact

VISEON is delivered as a three-stage model that mirrors how AI now interacts with the web.

### Discover

Make a brand instantly discoverable to AI agents. Audit Schema.org coverage across all domains, identify entity gaps, validate IDs and relationships, check Google Rich Result eligibility, and produce a comprehensive agentic catalogue that represents the business accurately.

**A-Audit:** Cross-domain schema artefacts → comprehensive, brand-representative agentic catalogue.

### Discuss

Replace traditional site search with AI-powered conversations grounded in a governed knowledge graph. Agents answer customer questions accurately, agent-to-agent or human-facing, in the brand voice.

**B-Build:** Governed Schema knowledge graph → foundation for intent-based semantic search, whether agent-to-agent or human.

### Transact

Connect the catalogue to commerce. Publish through structured data, APIs, MCP and NLWeb endpoints, and supported commerce protocols including ACP, AP2 and Google's Universal Commerce Protocol, so agents can browse, recommend and complete purchases.

**C-Connect:** Publish the catalogue and feed Ask-powered brand conversations and agentic transactions.

## Why This Matters

Many brands remain digitally obscure to AI systems because they lack structured context and authoritative signals. When customers ask an AI assistant for a recommendation, better-defined competitors are surfaced instead. Traditional SEO alone is no longer enough.

VISEON addresses this by exposing the cohesive knowledge graph of an entire digital presence: a digital twin, language model optimised. The platform audits Schema.org markup, validates JSON-LD framework compliance, verifies Google Rich Results, and enables hybrid Vector and GraphRAG semantic search via the Model Context Protocol.

## Standards and Protocols

VISEON is built on, and aligns to, open standards:

- **Schema.org** as the canonical vocabulary
- **JSON-LD** as the preferred serialisation, consistent with Google guidance and Microsoft NLWeb
- **Model Context Protocol (MCP)** for governed, deterministic agent access
- **NLWeb** for site-level conversational interfaces
- **ACP, AP2 and Google UCP** for agentic commerce flows
- **YAML-LD and DCAT 3** application profiles for dataset description

- ## Discovery Signals on VISEON.IO

VISEON.IO implements the same agent discovery signals it audits for clients. Every page exposes:

- A `<link rel="alternate" type="application/ld+json">` element pointing to the VISEON Knowledge Graph Catalog at `/wp-json/viseon/v1/catalog`, surfaced both in the HTML head and as an HTTP `Link:` header per RFC 8288.
- A site-level `schema.txt` discovery file at the domain root, conforming to the schematxt v4 specification, also surfaced as an HTTP `Link:` header.

Together these let crawlers, AI agents and MCP-enabled clients locate the canonical structured data without scraping rendered HTML.

## Capabilities

- Cross-domain Schema.org audit and validation against the latest specifications
- Entity disambiguation through `sameAs`, `knowsAbout` and `Organization` patterns
- Google Rich Result eligibility checks across retained schema types
- Knowledge graph completeness, accuracy and reachability scoring
- FUSEON APIs for programmatic access to schema and entity data
- MCP-ready data layer for direct agent consumption
- Hybrid Vector and GraphRAG retrieval for semantic search

## Who VISEON Is For

- Growing enterprises that need a rapid, hands-off deployment of an AI discovery strategy
- B2B organisations whose buyers research and shortlist vendors through AI assistants
- International brands that require entity consistency across multiple regional domains
- Institutions and content creators that need to protect intellectual property through semantic personification

## Repository Contents

- `README.md`: this file
- `Schema.org-JSON-LD-Edge-Integrity-Test.md`: public reference for evaluating JSON-LD edge-case integrity in Schema.org implementations

## Built by Differentia Consulting

VISEON is developed by [Differentia Consulting](https://www.differentia.consulting/), an 18-year Qlik Elite Partner that has been helping organisations prepare quality data models for business intelligence and AI use cases since 2002.

VISEON forms the AI discoverability layer of the [Smarter.BI](https://www.differentia.consulting/smarter.bi/) solution family. The Qlik-powered audit and governance interface is delivered as [Smarter.SEO](https://www.differentia.consulting/smarter.bi/solutions/smarter-seo-powered-by-qlik/).

## Getting Started

- **Website:** [viseon.io](https://viseon.io)
- **AI Discoverability Assessment:** [viseon.io/ai-discoverability-assessment](https://viseon.io/ai-discoverability-assessment/)
- **Glossary:** [viseon.io/terms](https://viseon.io/terms/)
- **Articles:** [viseon.io/articles](https://viseon.io/articles/)
- **Contact:** info@viseon.io
- **Phone:** +44 1494 622 600

## Connect

- **X:** [@VISEONIO](https://x.com/VISEONIO)
- **Reddit:** [r/viseon](https://www.reddit.com/r/viseon/)
- **GitHub Organisation:** [VISEONIO](https://github.com/VISEONIO)

---

Copyright © 2026 [Differentia Consulting Ltd](https://www.differentia.consulting/). All rights reserved.
