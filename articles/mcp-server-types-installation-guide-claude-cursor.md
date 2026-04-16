# How to Install Any MCP Server in Claude: The Complete Setup Guide

**URL:** https://buildtolaunch.substack.com/p/mcp-server-types-installation-guide-claude-cursor
**Track:** AI Agent Systems
**Published:** 2026-03-22

## Summary

MCP servers come in three connection types — stdio, HTTP, and OAuth — and each installs differently across Claude Desktop, Claude Code, and Cursor. This guide maps each type to its installation steps, config file locations, and the JSON format required for each platform.

Stdio servers run as local processes and communicate over standard input/output. They are the most common type for local tools (filesystem access, database clients, local scripts) and install via a command entry in the platform config. HTTP servers expose a remote endpoint and connect via URL; they work across machines and are common for SaaS integrations. OAuth servers add an authorization layer on top of HTTP, requiring a browser-based authentication step before the MCP can be used.

Config file locations differ by platform: Claude Desktop uses `~/Library/Application Support/Claude/claude_desktop_config.json` on macOS, Claude Code uses `.claude/settings.json` in the project root or `~/.claude/settings.json` globally, and Cursor uses `.cursor/mcp.json`. The article includes the exact JSON structure for each, with working examples that show how command, args, and env fields map to real MCP installations.

The guide also covers the most common connection errors — server not found, auth failures, tool not appearing in Claude — and the diagnostic steps to resolve each.

## Key Sections

- Three MCP connection types: stdio, HTTP, OAuth — when each applies
- Claude Desktop config: file location and JSON format
- Claude Code config: project-level vs. global settings
- Cursor MCP config: `.cursor/mcp.json` structure
- Working JSON examples for each platform and connection type
- Common installation errors and how to fix them
- How to verify an MCP server is connected and tools are available
