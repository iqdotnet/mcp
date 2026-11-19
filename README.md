# IQ.NET

IQ.NET is the search index for MCP servers, Apify actors and x402 endpoints (not io.net, Microsoft Work IQ, or the IQNet certification network).

Agents search the catalogue, then open a service to read the endpoint and the price its provider advertised. Search is free and needs no signup. IQ.NET does not call those services, hold a wallet, or take a payment. Some tools in the index are featured, and some listings include partner links.

Website: https://iq.net
Docs: https://iq.net/docs

## Connect the MCP server

The hosted server speaks Streamable HTTP at `https://api.iq.net/mcp`. There is no authentication. Tools: `search_services`, `get_service`.

**Claude Code**

```bash
claude mcp add --transport http iqnet https://api.iq.net/mcp
```

**mcp.json** (Cursor, VS Code, and similar)

```json
{
  "mcpServers": {
    "iqnet": {
      "url": "https://api.iq.net/mcp"
    }
  }
}
```

Claude.ai and ChatGPT can add the same URL as a connector.

## Other ways to use the index

- REST: `GET https://api.iq.net/v1/services?q=weather`
- OpenAPI: https://api.iq.net/openapi.json
- Skill: https://iq.net/SKILL.md
- llms.txt: https://iq.net/llms.txt

## Catalogue

Listings come from the official MCP Registry, the Coinbase x402 Bazaar, the Apify Store, curated GitHub projects, and reviewed submissions. An MCP listing is not an x402 listing. A GitHub repository is not a callable endpoint. As of 18 November 2026 the stats API reported 51,912 services.

This repository documents the hosted server. It is not a local install package.
