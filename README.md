# @pipeworx/data-europa

[data.europa.eu](https://data.europa.eu) MCP — official open-data portal of the European Union (~1.6M datasets aggregated from EU institutions and 27 member states). CKAN-compatible API. Keyless.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1394+ live data sources.

## Tools

- `search(query, fq?, rows?, start?, sort?)` — package search
- `package(id)` — single package by id
- `organizations(limit?)` — list publishing organizations
- `groups(limit?)` — list themes/groups
- `tags(query?, limit?)` — list/search tags

## Data source

`https://data.europa.eu/api/hub/search/`

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-europa": {
      "url": "https://gateway.pipeworx.io/data-europa/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1394+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Europa data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [Docs and guides](https://pipeworx.io/docs)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
