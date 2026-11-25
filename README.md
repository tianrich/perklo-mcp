# Perklo MCP Server
[![Listed in Awesome MCP Servers](https://sagargupta.online/awesome-mcp-servers/badge.svg)](https://github.com/Sagargupta16/awesome-mcp-servers)

Live UK deals, global voucher codes and ticket announcements, over MCP.

Connect your AI agent to Perklo and it can search real deals, check voucher codes and find ticket announcements, with live prices. No API key needed.

- **Endpoint:** `https://www.perklo.lol/mcp`
- **Protocol:** `2025-11-25`
- **Tools:** 27
- **Auth:** none — no key, no sign-up
- **Docs:** https://www.perklo.lol/developers

## What it gives your agent

- **Deals:** search live UK deals by product, store or price, and get a single deal with its price, was-price and tracked link.
- **Vouchers:** search voucher codes by store or country. Codes are international: US, UK, Germany, Austria and Switzerland.
- **Tickets:** search and list ticket announcements (concerts, tours) with on-sale dates and tracked ticket links.
- **Checks:** precheck a deal to see if it is still live and at the stated price, and wrap any URL in the right affiliate form.

Every link the server returns is a Perklo-tracked link (`/go/<id>`, `/voucher/go/<hash>`, `/tickets/go/<id>`).

## Connect

Add this to your MCP client config:

```json
{
  "mcpServers": {
    "perklo": {
      "url": "https://www.perklo.lol/mcp"
    }
  }
}
```

For clients that need a local bridge (Claude Desktop), use `mcp-remote`:

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

See `llms-install.md` for client-by-client setup, and https://www.perklo.lol/developers for the full tool list.

## Links

- Website: https://www.perklo.lol
- Developers: https://www.perklo.lol/developers
- llms.txt: https://www.perklo.lol/llms.txt
- MCP endpoint: https://www.perklo.lol/mcp
