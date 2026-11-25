# Install Perklo MCP

Connect an AI agent or MCP client to Perklo's hosted MCP server. No API key, no sign-up. The server speaks Streamable HTTP at `https://www.perklo.lol/mcp` (protocol `2025-11-25`).

## Quick config

Most clients take a `mcpServers` entry. Use the direct URL where the client supports remote servers:

```json
{
  "mcpServers": {
    "perklo": {
      "url": "https://www.perklo.lol/mcp"
    }
  }
}
```

## Claude Desktop (via mcp-remote)

Claude Desktop needs a local bridge. Install with:

```json
{
  "mcpServers": {
    "perklo": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://www.perklo.lol/mcp"]
    }
  }
}
```

## Cursor (one click)

Add this to Cursor's MCP settings, or use the one-click install on https://www.perklo.lol/developers.

```json
{
  "mcpServers": {
    "perklo": {
      "url": "https://www.perklo.lol/mcp"
    }
  }
}
```

## VS Code / Windsurf

Same `mcpServers` entry as above, in the client's MCP settings file.

## What the server offers

27 tools, 5 resources, 5 prompts. The main ones:

- `search_deals` — live UK deals by product, store or price
- `get_deal` — one deal with price, was-price and tracked link
- `search_vouchers` — voucher codes by store or country (US, GB, DE, AT, CH)
- `search_ticket_announcements` — ticket announcements with on-sale dates
- `precheck_deal` — is the deal still live, and at the stated price
- `wrap_link` — wrap any URL in the right affiliate form

Full tool list and docs: https://www.perklo.lol/developers
