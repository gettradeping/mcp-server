# Lead generation by Tradeping

Lead generation MCP server for Claude Desktop, Cursor or any MCP client. [Tradeping](https://gettradeping.com) finds B2B leads from fresh job posts: roofing leads, HVAC leads, real estate leads and mortgage leads at companies that are hiring right now. Each lead comes with the decision maker, a verified email and a drafted first message, ready for cold email outreach from your own mailbox.

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

## Contact data: sources, legal basis and opt-out

Leads are business contacts only: the company comes from public job posts and its public business listing, and the decision maker's name, job title and verified work email come from business-contact data providers. Tradeping holds this data for one-to-one business-to-business outreach on the basis of legitimate interests (Article 6(1)(f) GDPR). Anyone listed can be removed at once, for every customer, at https://gettradeping.com/opt-out/.

MIT license
