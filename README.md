# perplexity-mcp

Tiny Python MCP server for Perplexity web search — 3 tools with escalating depth.

## Tools

| Tool | Speed | Use for |
|------|-------|---------|
| `web_search(query)` | 2-5s | Quick facts, simple lookups |
| `web_ask(query)` | 5-15s | Thorough answers, literature discovery |
| `deep_research(query)` | 2-10 min | Comprehensive multi-step analysis |

Both `web_search` and `web_ask` accept optional `focus` (`"academic"`, `"finance"`) and `recency` (`"day"`, `"week"`, `"month"`, `"year"`) parameters.

## Setup

```bash
pip install -e .
export PERPLEXITY_API_KEY=pplx-...
perplexity-mcp  # starts stdio MCP server
```

## MCP client config

```json
{
  "name": "perplexity",
  "cmd": ["perplexity-mcp"],
  "env": {"PERPLEXITY_API_KEY": "pplx-..."}
}
```
