# Asia Miles Calculator MCP Server

A free **remote MCP server** for Cathay Pacific's **Asia Miles** program. Calculate how many Asia Miles you need for award flights — including **mixed-cabin** itineraries, where each segment is prorated by great-circle distance — validate routes against Cathay Pacific and oneworld partner networks, search airports, and look up direct routes.

**Endpoint:** `https://asiamiles-calculator.site/api/mcp` (Streamable HTTP, no API key, no sign-up)

**Docs:** https://asiamiles-calculator.site/mcp · **Official MCP Registry:** `io.github.yshkk/asia-miles-calculator`

## Connect

Clients that support remote MCP servers (Claude, Cursor, VS Code, …):

```json
{
  "mcpServers": {
    "asia-miles-calculator": {
      "url": "https://asiamiles-calculator.site/api/mcp"
    }
  }
}
```

stdio-only clients, via [mcp-remote](https://www.npmjs.com/package/mcp-remote):

```json
{
  "mcpServers": {
    "asia-miles-calculator": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://asiamiles-calculator.site/api/mcp"]
    }
  }
}
```

## Tools

| Tool | Description |
|---|---|
| `calculate_asia_miles` | Mileage for 1–2 segment itineraries: Economy, Business and proportional Mixed-Cabin plans, distances, route validation |
| `search_airports` | Search airports by IATA code, city or airport name (English & Chinese) |
| `get_direct_routes` | Direct routes from an airport, with operating airlines and seasonality |

## Example prompts

- "How many Asia Miles do I need from Hong Kong to Tokyo in business class?"
- "Compare economy, business and mixed-cabin options from Beijing to Phuket via Hong Kong."
- "Which airlines fly direct from Hong Kong to Osaka?"

## About

Asia Miles Calculator (https://asiamiles-calculator.site/) is an independent tool for Asia Miles members. Not affiliated with Cathay Pacific. Mileage figures follow the current Asia Miles award chart and are estimates; taxes and carrier surcharges are extra.

## License

MIT
