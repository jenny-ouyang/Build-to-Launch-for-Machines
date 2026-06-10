# MCP Servers in Every AI Client: Claude, ChatGPT, VS Code, and Cursor

**URL:** https://buildtolaunch.substack.com/p/mcp-setup-claude-chatgpt-vscode-cursor
**Track:** AI Builders Playbook
**Published:** 2026-03-17

## Summary

Most MCP setup guides stop at Claude Desktop, or at most add Claude Code. This one covers all seven places a builder might want MCP servers: Claude Desktop, Claude Code, ChatGPT Desktop, Cursor, Windsurf, VS Code with GitHub Copilot, and remote OAuth connectors. Each client has its own config file, its own path, and its own behavior when something breaks, so the article treats them as seven separate setups with exact snippets rather than one generic procedure.

It starts with the concept that determines everything downstream: MCP transport types, stdio versus HTTP/SSE, and why the choice matters before you edit any config. From there it walks Claude Desktop end to end — where the config file lives, what it looks like, the required restart, the three install routes (npm, Python, local), and troubleshooting — then does the same for Claude Code via the CLI, including the `claude mcp add` command and the user-scope versus project-scope decision.

A large middle section handles the realities of working on a team and across editors. It shows how to share MCP config with `.mcp.json`, how to store API keys safely inside a shared config, and how `.mcp.json` differs from `.claude/settings.json`. Then it repeats the exact-config treatment for Cursor and Windsurf, remote connectors through Claude, ChatGPT, and VS Code with Copilot — each with its own enabling steps and troubleshooting notes.

The closing sections are decision support rather than instructions: Cursor versus VS Code for MCP, whether the same server can run across all clients, how to migrate config from one editor to another, how to verify a connection is actually working, an install-command reference for npm, Python, and Docker, which servers to install first, and a starter `.mcp.json` template. The throughline is a decision table that routes a reader to the right method for their setup instead of forcing one path.

## Key Sections

- MCP Transport Types: stdio vs HTTP/SSE
- How to Add MCP Servers to Claude Desktop (config location, install routes, troubleshooting)
- How to Add MCP Servers to Claude Code (CLI Method, user vs project scope)
- How to Share MCP Config Across a Team (.mcp.json) and store API keys safely
- How to Set Up MCP Servers in Cursor and Windsurf
- How to Add a Remote MCP Server via Claude Connectors
- How to Add MCP Servers to ChatGPT
- How to Set Up MCP in VS Code with GitHub Copilot
- Cursor vs VS Code for MCP, migration, verification, and a starter template
