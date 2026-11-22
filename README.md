# Tradeping MCP server

Use [Tradeping](https://gettradeping.com) from Claude Desktop, Cursor or any MCP client: companies in roofing, HVAC, real estate and mortgage that are hiring right now, the decision maker, a verified email and a drafted first message.

## Remote (recommended)

Add `https://gettradeping.com/mcp` as a custom connector (Streamable HTTP, OAuth). In Claude Code:

```sh
claude mcp add --transport http tradeping https://gettradeping.com/mcp
```

Clients without OAuth can send a Tradeping API key as `Authorization: Bearer tp_live_…` (Settings → API keys).

## Desktop package

```sh
npx -y tradeping-mcp
```

The package is a thin bridge to the remote server; your browser opens once for sign-in and consent.

## Tools

`get_account`, `list_leads`, `get_lead`, `find_leads`, `update_lead`, `rewrite_lead`, `send_lead`, `list_suppressions`, `add_suppression`. Every tool uses your plan's limits, like the web app. Full docs: https://gettradeping.com/developers/

MIT license
