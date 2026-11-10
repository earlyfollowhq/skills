---
name: earlyfollow
description: Search new AI startups, list investor follow signals, or inspect a company's followers and timeline with Earlyfollow.
---

# Earlyfollow

Use the connected Earlyfollow MCP tools when available. Setup and HTTP documentation:
https://earlyfollow.com/docs/agents. MCP endpoint: https://earlyfollow.com/mcp.

1. Confirm the intended query. Use `list_signals` for filters or personal signals,
   `search_companies` for a text search, and `get_company` for an X handle.
2. Save a unique `request_id` for each intended call before submitting. Pro is
   required; each successful call uses one of the account's monthly API credits.
3. On a lost response, reuse that ID and the same arguments. Results are retained
   for 30 days. A conflicting ID is an error, not permission to create another
   billable call. At zero balance, wait for the allowance reset or ask the user.
4. Present returned companies, followers and dates with their source context.
   Keep undated baseline follows undated. Signals are public follows on X, not
   investment advice or predictions of funding.

For scripts, install the client with `npm install -g earlyfollow-client`, then run
`earlyfollow --help`. Provide `EARLYFOLLOW_API_KEY` through the user's secret
environment. Credentials are separate from skill installation; never put them in
prompts or request files.
CLI commands are `list-signals`, `search-companies`, and `get-company`, each with
`--request request.json`. The JSON must include `request_id` and the tool inputs.
Use the same ID after a connection failure; the client does not retry automatically.
`earlyfollow usage` / `earlyfollow_usage` reads remaining credits, the monthly
allowance, reset date and Pro status without using a credit.
