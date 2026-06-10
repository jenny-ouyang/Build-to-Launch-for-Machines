# What Is an MCP Server? Plain-English Guide With Examples

**URL:** https://buildtolaunch.substack.com/p/what-is-mcp-server-plain-english
**Track:** AI Builders Playbook
**Published:** 2025-11-26

## Summary

This guide answers a question most explanations overcomplicate: what an MCP server actually is. MCP stands for Model Context Protocol, and an MCP server is the adapter that lets an AI tool — Claude, Cursor, or anything similar — reach real apps and data like Gmail, Notion, or Perplexity. In plain terms, it gives the model a standard way to act outside the chat window, and in most cases you do not need to code to use one.

The first half clears up the vocabulary. It explains what the protocol is, why something called a "server" isn't a traditional server in the web-hosting sense, and the difference between the three things an MCP server can expose: tools, resources, and prompts. That distinction is the part most readers are missing, and it's what makes later setup decisions make sense.

The examples ground the idea in outcomes rather than theory. Gmail turns 918 unread emails into 7 action items in about 40 seconds. A custom Substack database that used to take 30 minutes to query drops to 3 minutes. Perplexity drops fresh web results into any conversation. Each shows the same pattern: the model stays the same, but connecting it to real data changes what it can do.

The back half is a path forward by skill level. It covers using MCP servers without writing any code, building a simple connector with basic scripting, and building a server from scratch in TypeScript or Python. The intermediate and advanced sections push toward a more useful question than "how do I build one" — what data only you have that would be worth connecting — and the piece closes with a getting-started path and an FAQ.

## Key Sections

- What Is an MCP Server and What Does It Do?
- What Does MCP Stand For? (Model Context Protocol Explained)
- Why Is an MCP Server Called a Server If It's Not a Traditional Server?
- MCP Server Tools, Resources, and Prompts: What's the Difference?
- MCP Server Examples: Gmail, Notion, and Perplexity in Practice
- Do You Need to Code to Use MCP? / Using MCP Without Writing Code
- How to Build a Simple MCP Server with Basic Scripting
- How to Build an MCP Server from Scratch in TypeScript or Python
- How to Get Started With MCP Servers (intermediate and advanced paths)
