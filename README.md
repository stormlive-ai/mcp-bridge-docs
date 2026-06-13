# MCP-Bridge

**Convert any OpenAPI spec to an MCP server config — in your browser.**

MCP-Bridge is a free tool that lets you browse 500+ APIs, generate ready-to-use Model Context Protocol (MCP) server configurations, and download them for Claude Desktop, Cursor, or any MCP-compatible client.

**[Launch the App →](https://mcpbridge.org)**

## Features

- **Browser-based converter** — Paste any OpenAPI spec (JSON/YAML), get an MCP config instantly. No data leaves your browser.
- **500+ API directory** — Browse APIs by category: AI/ML, Cloud, Finance, Communication, Databases, and more.
- **One-click configs** — Ready-to-use MCP configs for Claude Desktop, Cursor, and other MCP hosts.
- **Framework rules** — 25+ .cursorrules templates for popular frameworks.
- **Free and open** — No signup, no backend, no cost.

## Quick Start

1. **Visit** [mcpbridge.org](https://mcpbridge.org)
2. **Browse** the API directory or use the converter
3. **Generate** your MCP config
4. **Copy** the JSON into your `claude_desktop_config.json` or Cursor MCP settings

## What is MCP?

Model Context Protocol (MCP) is an open standard that connects AI assistants with external tools and data sources. It lets Claude, Cursor, and other AI agents interact with APIs, databases, and services through a standardized interface.

## Repository Structure

```
mcp-bridge-docs/
├── README.md              # This file
├── LICENSE                # MIT License
├── CODE_OF_CONDUCT.md     # Community standards
├── CONTRIBUTING.md        # How to contribute
└── docs/
    └── openapi-to-mcp.md  # Converter tool guide
```

## Tech Stack

The main site (private repo) is built with:

- **Next.js 16** — Static site generation
- **TypeScript** — Full type safety
- **Tailwind CSS** — Utility-first styling
- **APIs.guru** — OpenAPI specification directory
- **Cloudflare Pages** — Hosting and CDN

## License

MIT

---

Built by [stormlive-ai](https://github.com/stormlive-ai)
