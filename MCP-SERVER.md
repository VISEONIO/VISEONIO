# VISEON MCP server: developer guide

Registry identifier: `io.viseon/semantic-intelligence`  
Remote server: **VISEON for Web**  
Endpoint: **https://viseon.io/mcp**  
Transport: **Streamable HTTP over HTTPS**

Connect an MCP client to query VISEON's public Schema.org knowledge graph: its organisation, products, services, people, FAQs, glossary terms and articles, with their relationships and source URLs. This public endpoint exposes knowledge retrieval tools. It does not provide access to private customer systems or perform enterprise transactions.

## Authentication and access

The public endpoint requires **no API key, OAuth login, VISEON account or paid plan**. Public queries are available free of charge. Your chosen AI client may have its own account, subscription or organisation policy requirements.

Commercial VISEON services for building and governing an organisation's own graph are described on the [pricing page](https://viseon.io/pricing/); purchasing those services is not required to query this public server. Private enterprise deployments have their own access requirements.

## Connect from VS Code / GitHub Copilot

Create `.vscode/mcp.json` in your workspace with:

```json
{
  "servers": {
    "viseon": {
      "type": "http",
      "url": "https://viseon.io/mcp"
    }
  }
}
```

Start the server using VS Code's MCP controls and approve the server trust prompt if shown. In Copilot Chat, select an agent mode that can use MCP tools and enable the VISEON tools. If your organisation manages MCP access, it may need to allow this server.

For other clients supporting remote Streamable HTTP MCP servers, enter `https://viseon.io/mcp` as the server URL and leave authentication unset. Configuration field names vary by client.

## Tools

Tool names below are the exact names returned by `tools/list`.

| Tool | Purpose | Inputs |
| --- | --- | --- |
| `fuzzy_find_and_traverse` | Find and rank entities from natural language, including alternative names and spelling variations; returns entity context and relationship IDs. | Required: `query`. Optional: `type`, `limit` (1–10, default 5), `detail` (`summary` or `full`), `weights`. |
| `get_entity` | Retrieve complete Schema.org entity data and relationships held in either direction. | Required: `url`, the entity's `@id`. |
| `query_relationships` | List a subject's property values and linked entities, optionally filtered by predicate. | Required: `subject`. Optional: `predicate`. |
| `find_by_type` | Find entity IDs with an exact Schema.org type, such as `Service`, `Person` or `DefinedTerm`. | Required: `type`. |
| `search_content` | Run a substring search across entity text; returns up to 20 entity URLs. | Required: `query`. |
| `traverse_path` | Follow a chain of graph relationships from an entity ID or name; prefix a predicate with `^` to follow it backwards. Returns edges, literal values and truncation information. | Required: `start`. Optional: `path` (up to three hops, each a predicate or list of predicates), `maxHops` (1–3, default 2). |
| `get_citable_passages` | Retrieve verbatim article passages with passage and article links for quotation and citation. | Required: `query`. Optional: `article` (entity ID, page URL or title), `limit` (1–5, default 3). |

Start natural-language discovery with `fuzzy_find_and_traverse`, then use `get_entity` for full details or `traverse_path` for a known relationship chain. Use `get_citable_passages` when an answer needs an article quotation; an article entity's description is not its complete text.

Results are returned in `structuredContent`. The server varies its text representation and default discovery detail with the negotiated protocol version. Set `detail` explicitly when a particular discovery representation is needed. Respect returned truncation indicators and follow entity IDs for additional detail.

## Resources and prompt templates

This endpoint currently advertises **tools only**. It exposes no MCP resources, resource templates or server-defined prompt templates. `resources/list` and `prompts/list` return JSON-RPC method-not-found errors (`-32601`). The example prompts below are requests to your AI client, not server-defined MCP prompts.

The [full graph JSON-LD download](https://viseon.io/wp-json/viseon/v1/graph) is a separate HTTP dataset, not an MCP resource.

## Example prompts and use cases

- **Product discovery:** “Use VISEON to explain VISEON for Web, identify its related services and include the source URLs.”
- **Compare offerings:** “Using VISEON's graph, compare VISEON for Web and VISEON for Enterprise. Base the comparison on the registered entities and cite their source pages.”
- **Understand terminology:** “Find VISEON's definition of Semantic Entity Optimisation and show the related concepts.”
- **Source-backed research:** “Find article passages about knowledge graphs, quote the relevant wording and link to each passage.”

For a direct tool call, discover entities with:

```json
{
  "name": "fuzzy_find_and_traverse",
  "arguments": {
    "query": "VISEON for Web",
    "limit": 3,
    "detail": "summary"
  }
}
```

This is the `params` object for MCP `tools/call`, after the client has completed MCP initialisation. Follow a returned entity ID with `get_entity` using that ID as `url`.

## Discovery and verification

- [Agentic Resource Discovery (ARD) manifest](https://viseon.io/.well-known/ard.json): machine-readable discovery metadata and representative queries.
- [VISEON Ask](https://viseon.io/ask/): a human-facing interface to the graph.
- [VISEON](https://viseon.io/): platform information.

The ARD complements this developer guide. Use the live MCP `initialize` and `tools/list` responses as the authority for currently exposed MCP capabilities; discovery metadata can lag tool additions.

Verified against the public endpoint on **28 October 2026**: successful unauthenticated MCP initialisation using protocol `2025-03-26`, seven tools returned by `tools/list`, and no resources or prompt templates advertised. The endpoint accepts MCP JSON-RPC requests by HTTP POST with `Content-Type: application/json` and `Accept: application/json, text/event-stream`. Opening the endpoint as an ordinary web page may return HTTP 405; use an MCP client to connect.

Support: **info@viseon.io** or the [VISEON contact page](https://viseon.io/contact/).
