# MCP-Bridge — OpenAPI to MCP Converter & Server Directory

**Browser-based OpenAPI → MCP conversion. 500+ API configs. 400+ MCP servers indexed. 27 framework rules. Zero backend.**

[![Website](https://img.shields.io/badge/Website-mcpbridge.org-blue)](https://mcpbridge.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**[mcpbridge.org](https://mcpbridge.org)** — The fastest way to connect any REST API to AI assistants like Claude Desktop, Cursor, and Cline. Paste your OpenAPI v3 spec and get a ready-to-use MCP server configuration instantly — all in your browser, no data leaves your machine.

## What is MCP-Bridge?

MCP-Bridge is a complete platform for the Model Context Protocol (MCP) ecosystem:

| Feature | Description | Link |
|---------|-------------|------|
| **OpenAPI → MCP Converter** | Paste any OpenAPI v3 JSON/YAML spec, get MCP config in seconds | [Try it](https://mcpbridge.org/convert) |
| **API Config Directory** | 500+ pre-built MCP configurations for popular APIs | [Browse](https://mcpbridge.org/directory) |
| **MCP Server Index** | 400+ native MCP servers with quality scores and health checks | [Explore](https://mcpbridge.org/directory?tab=mcp-servers) |
| **Server Comparison** | Compare MCP servers side-by-side by features, stars, and score | [Compare](https://mcpbridge.org/compare-servers) |
| **Framework Rules** | 27 .cursorrules files for Cursor AI optimization | [Download](https://mcpbridge.org/directory?tab=frameworks) |
| **Blog & Guides** | 21 tutorials on MCP setup, security, and integration | [Read](https://mcpbridge.org/blog) |

## Why MCP-Bridge?

- **Zero backend** — The converter runs entirely in your browser. Your API specs never touch a server.
- **No signup** — No accounts, no payments, no data collection.
- **Privacy by design** — All parsing is local. Enterprise-grade security without enterprise complexity.
- **Comprehensive** — From GitHub and Stripe to PostgreSQL and Figma — one platform for all MCP needs.

## Getting Started

```bash
# 1. Go to mcpbridge.org
# 2. Find your API or paste an OpenAPI spec
# 3. Copy the generated MCP config
# 4. Add to your MCP client:
```

### Claude Desktop
Add to `claude_desktop_config.json`:
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "your-token-here"
      }
    }
  }
}
```

### Cursor
Add to `.cursor/mcp.json` in your project root.

### VS Code
Use with any MCP-compatible VS Code extension.

## Supported APIs (Sample)

GitHub, Stripe, Slack, PostgreSQL, Notion, Figma, OpenAI, Supabase, Cloudflare, Discord, Linear, Sentry, Datadog, PagerDuty, Jira, Confluence, Okta, Auth0, and 500+ more.

## What is MCP?

The Model Context Protocol (MCP) is an open standard that connects AI assistants with external tools and data sources. Think of it as USB-C for AI — a universal protocol that lets any AI client talk to any backend service. Learn more in our [complete MCP guide](https://mcpbridge.org/blog/what-is-mcp).

## Repository Structure

```
mcp-bridge-docs/
├── README.md          # This file
├── LICENSE            # MIT License
├── CODE_OF_CONDUCT.md # Community standards
├── CONTRIBUTING.md    # How to contribute
└── docs/
    └── openapi-to-mcp.md  # Converter tool guide
```

## Related Repositories

- [mcp-bridge](https://github.com/stormlive-ai/mcp-bridge) — Main website source (Next.js 16, TypeScript, Tailwind CSS)
- [mcp-bridge-parser](https://github.com/stormlive-ai/mcp-bridge-parser) — Core OpenAPI → MCP parsing library (npm: `mcp-bridge-parser`)

## License

MIT — see [LICENSE](LICENSE).

---

Built by [stormlive-ai](https://github.com/stormlive-ai).  
Website: [mcpbridge.org](https://mcpbridge.org)
