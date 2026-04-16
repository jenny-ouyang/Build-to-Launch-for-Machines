# The Custom MCPs Included in Your Build to Launch Subscription

**URL:** https://buildtolaunch.substack.com/p/custom-mcps-claude-code-cursor
**Track:** AI Agent Systems
**Published:** 2026-04-12

## Summary

Build to Launch ships a set of custom MCP servers to paid subscribers that cover the four main workflow areas Jenny uses daily: research, writing/Substack, Gmail, and content distribution. This article documents what each MCP does, which tools it exposes, and how to wire it into Claude Code or Cursor.

The research MCP connects Perplexity search directly into the Claude Code context window, so competitive research, fact-checking, and topic exploration happen without breaking the coding session to open a browser. The Substack MCP handles reading drafts, fetching subscriber data, and managing notes from within Claude. The Gmail MCP enables multi-account email management — the same tool covered in depth in the Gmail MCP setup article — allowing inbox triage, morning briefs, and subscriber tracking without switching to the Gmail web interface.

The distribution MCP covers the publishing pipeline: cross-posting to Dev.to, formatting for different platforms, and triggering the distribution workflow from a single Claude prompt. Each MCP is installable from the Build to Launch GitHub repository and comes with a setup guide for both Claude Code (via `.claude/settings.json`) and Cursor (via `mcp.json`).

## Key Sections

- Overview of the 4 custom MCPs: research, Substack, Gmail, distribution
- Perplexity MCP: research without leaving Claude Code
- Substack MCP: draft management and subscriber data tools
- Gmail MCP: multi-account inbox management from Claude
- Distribution MCP: cross-platform publishing automation
- Installation instructions for Claude Code and Cursor
- How to access the MCPs as a paid Build to Launch member
