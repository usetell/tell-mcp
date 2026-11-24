# Tell MCP server

[Tell](https://usetell.dev) is agentic outreach: connect Claude (or any MCP client) and it finds the right people, verifies their work emails, writes an opening line from what each company is doing, and sends sequences from your own inbox. Follow-ups stop when someone replies, and nothing sends until you approve it.

This repository holds the registry metadata for Tell's hosted MCP server. The server itself runs at:

```
https://usetell.dev/mcp
```

Streamable HTTP with OAuth. Sign in with your Tell account when your client asks.

## Connect

Claude Code:

```
claude mcp add --transport http tell https://usetell.dev/mcp
```

Claude.ai and Claude Desktop: Settings, Connectors, Add custom connector, paste `https://usetell.dev/mcp`.

Any other MCP client:

```json
{ "mcpServers": { "tell": { "url": "https://usetell.dev/mcp" } } }
```

## Tools

| Tool | What it does |
| --- | --- |
| enrich_lead | Verified work email, what the company sells, a buying signal and an opener for one person |
| enrich_list | The same for a list of people |
| get_run, list_runs | Progress and results of list runs |
| search_leads, get_lead | Find and read researched leads |
| watch_company | Watch a company for hiring, funding, launches, pricing and App Store rating changes |
| list_signals | Fresh buying signals from watched companies |
| create_sequence | Draft a multi-step email sequence (nothing sends yet) |
| start_sequence, pause_sequence | Start after your approval, or pause |
| list_sequences | Sequences and their results |
| get_account | Credits and connected mailboxes |

## Pricing

One credit per verified email found. Misses are free, and every workspace starts with 10 free credits. See [usetell.dev](https://usetell.dev).

Questions: hello@usetell.dev
