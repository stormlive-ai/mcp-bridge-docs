# OpenAPI to MCP Converter Guide

The MCP-Bridge converter lets you convert any OpenAPI specification to a ready-to-use MCP server configuration — entirely in your browser.

## How It Works

1. **Input**: Paste a JSON/YAML OpenAPI spec or upload a file
2. **Parse**: The browser parses all paths, methods, parameters, and schemas
3. **Generate**: Produces a `mcpServers` configuration block compatible with Claude Desktop, Cursor, and other MCP hosts
4. **Download**: Save the config or copy it directly

## Supported Input Formats

- **JSON** — Standard OpenAPI 3.x JSON format
- **YAML** — OpenAPI 3.x YAML format (via `js-yaml` parser)
- **URL** — Fetch a spec directly from a URL (CORS permitting)

## Example

**Input** (OpenAPI spec snippet):
```json
{
  "openapi": "3.0.0",
  "info": { "title": "Weather API", "version": "1.0.0" },
  "paths": {
    "/weather": {
      "get": {
        "summary": "Get current weather",
        "parameters": [
          { "name": "city", "in": "query", "required": true, "schema": { "type": "string" } }
        ]
      }
    }
  }
}
```

**Output** (MCP config):
```json
{
  "mcpServers": {
    "weather-api": {
      "command": "npx",
      "args": ["-y", "@mcp/weather-api"],
      "env": { "WEATHER_API_KEY": "your_api_key" }
    }
  }
}
```

## Privacy

All parsing happens client-side. No data is sent to any server. Your API specs never leave your browser.

## Tips

- For production APIs, use an API key or OAuth token in the `env` section
- Test your config by pasting it into Claude Desktop's `claude_desktop_config.json`
- Use the dropdown examples to see how popular APIs (Weather, Petstore, GitHub) convert
