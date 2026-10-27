# VISEON

**Semantic Intelligence** · Discover | Discuss | Transact

*AI agents can't execute on canonical truth until you define it.*

[VISEON](https://viseon.io) is a Semantic Control Plane (operating system for AI) for governing organisational meaning and evidence across enterprise systems, websites and AI interfaces. It serves as the Governed Navigator for enterprise AI, giving autonomous engines and LLMs the explicit pathways, guardrails and auditability required to discover, discuss and transact with precision.

This repository is the public reference for VISEON. The platform itself runs at [viseon.io](https://viseon.io), which is the canonical source for what VISEON is and does.

## One governed semantic ecosystem. Four complementary solutions.

Every VISEON solution is governed, built around authoritative business meaning, and MCP-addressable. All four solutions are live.

| Solution | What it does |
|---|---|
| [VISEON for Web](https://viseon.io/viseon-for-web/) | Makes your brand, organisation, products and services understandable to AI through a governed digital twin and knowledge graph, accessible to visitors through VISEON Ask and to AI agents through MCP. |
| [VISEON for Enterprise](https://viseon.io/viseon-for-enterprise/) | Establishes a governed Semantic Control Plane connecting enterprise systems, business definitions and relationships, giving AI agents authoritative context through MCP without replacing existing access controls. |
| [VISEON for Qlik (vCat)](https://viseon.io/viseon-for-qlik-vcat/) | Governs the meaning of your Qlik analytics estate, making applications, metrics, master items and business context discoverable and actionable by AI agents through MCP. |
| [VISEON Data Assurance](https://viseon.io/viseon-data-assurance/) | Establishes trust in enterprise data through governed quality, completeness and compliance checks, publishing verifiable evidence and data assurance status to AI agents through MCP. |

## Discover, Discuss, Transact

- **Discover.** VISEON audits what public and internal AI architectures can currently see, identifies critical context gaps, and registers verified, brand-aligned facts into a unified context layer.
- **Discuss.** Evidenced facts registered into a canonical context Ask/MCP layer let AI agents give accurate, authoritative answers across every touchpoint: web discovery, internal knowledge retrieval, or agent-to-agent execution.
- **Transact.** The registry is connected through MCP and transient feeds, such as live prices and stock through change data capture, so agents can discover, recommend and act on it.

## Semantic Entity Optimisation (SEO 3.0)

Semantic Entity Optimisation optimises the entity, not the page. Each thing an organisation is and offers gets one canonical definition, a stable identifier, verified links to the rest of the web and a record of where each fact came from, so AI reads the organisation from the source. It includes everything schema markup has always had to do, Google Rich Results included, and does not stop there.

[Smarter.SEO](https://www.differentia.consulting/smarter.bi/solutions/smarter-seo-powered-by-qlik/) is VISEON.IO for Qlik customers, existing and prospective, delivered by Differentia Consulting.

## VISEON runs on VISEON

viseon.io is built the way VISEON builds for clients. Every page, product, service, person, glossary term and FAQ is an entity in one governed graph, served to people and to agents:

- [VISEON Ask](https://viseon.io/ask/) answers visitors from the graph, with sources.
- An MCP endpoint at `viseon.io/mcp`.
- An Agentic Resource Discovery (ARD) manifest at [`/.well-known/ard.json`](https://viseon.io/.well-known/ard.json).
- A listing in the official MCP Registry as `io.viseon/semantic-intelligence`.
- The knowledge graph catalog at [`/wp-json/viseon/v1/catalog`](https://viseon.io/wp-json/viseon/v1/catalog) and a [`schema.txt`](https://viseon.io/schema.txt) entity index, both advertised in the HTTP `Link:` headers and `<link rel="alternate">` elements of every page.

## Built on open standards

Schema.org, JSON-LD, the Model Context Protocol, NLWeb and Agentic Resource Discovery (ARD), connected to open commerce protocols including ACP, AP2 and Google's Universal Commerce Protocol. The graph is portable, inspectable and yours.

## In this repository

- `README.md`: this file.
- [FAQ.md](FAQ.md): What does VISEON do?
- `Schema.org-JSON-LD-Edge-Integrity-Test.md`: a reference prompt for checking that a Schema.org `@graph` is fully connected by bidirectional edges.

## Other public repositories

| Repository | Purpose |
|---|---|
| [qonnect-fixtures](https://github.com/VISEONIO/qonnect-fixtures) | Synthetic test data for VISEON Qonnect and the VISEON DuckDB extension. No real customer data. |
| [templates](https://github.com/VISEONIO/templates) | Industry Schema.org JSON-LD templates, with example organisations. |
| [public_data](https://github.com/VISEONIO/public_data) | Reference data files used by VISEON tooling. |
| [agentfinder-catalog](https://github.com/VISEONIO/agentfinder-catalog) | Fork of GitHub's agent finder catalog, used to submit VISEON's MCP server and Differentia's services catalog upstream. |

## Built by Differentia Consulting

VISEON is developed by [Differentia Consulting](https://www.differentia.consulting/), enterprise data specialists since 2002 and a Qlik partner, who have been helping organisations prepare quality data models for business intelligence and AI. VISEON sits within the [Smarter.BI](https://www.differentia.consulting/smarter.bi/) solution family.

## Get started

- **Free Semantic Entity Assessment:** [viseon.io/semantic-entity-assessment](https://viseon.io/semantic-entity-assessment/)
- **Website:** [viseon.io](https://viseon.io)
- **Pricing:** [viseon.io/pricing](https://viseon.io/pricing/)
- **Problems VISEON solves, and how it compares:** [viseon.io/problems](https://viseon.io/problems/)
- **FAQ:** [viseon.io/faq](https://viseon.io/faq/)
- **Glossary:** [viseon.io/terms](https://viseon.io/terms/)
- **Articles:** [viseon.io/articles](https://viseon.io/articles/)
- **Contact:** info@viseon.io · +44 1494 622 600

## Connect

- **X:** [@VISEONIO](https://x.com/VISEONIO)
- **GitHub:** [VISEONIO](https://github.com/VISEONIO)

---

Copyright © 2026 [Differentia Consulting Ltd](https://www.differentia.consulting/). All rights reserved.
