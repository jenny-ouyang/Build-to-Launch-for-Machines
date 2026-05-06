# What Are MCP Apps, Connectors, and Plugins? The Ecosystem Explained

**URL:** https://buildtolaunch.substack.com/p/what-are-mcp-apps-connectors-plugins
**Track:** AI Builders Playbook
**Published:** 2026-05-06

## Summary

MCP went from one open protocol launched by Anthropic in November 2024 to a layered ecosystem in eighteen months. The vocabulary multiplied faster than the documentation: connectors, plugins, MCP Apps, A2A — none of them obviously related. This article is the architecture map. MCP is the foundation, the standard for how AI connects to external tools. Connectors are pre-built MCP servers exposed through product UIs (Claude.ai integrations, Microsoft Copilot Studio "connectors" — same thing, different brand). Plugins bundle MCP servers, skills, and commands into installable extensions. MCP Apps, launched January 2026, extend the protocol so tools can return interactive UI directly inside the chat window. They don't compete. They stack.

The article also unpacks the three MCP primitives most people miss: tools (executable functions, model-driven), resources (read-only data, application-driven), and prompts (reusable templates with slash commands). Knowing the difference changes how you evaluate trust — a resource server reading your calendar needs less vetting than a tool server that can write to it.

The ecosystem passed 10,000 servers in April 2026, but an audit of 1,847 servers found 52% abandoned, 31% lightly maintained, and only 17% production-ready. Trending lists make selection harder, not easier. The filter that works: don't install from lists, install from friction. Find the tab you keep switching to manually and pick the MCP that eliminates that switch.

A2A (Agent-to-Agent) is the second protocol entering the picture. Where MCP handles AI-to-tool, A2A handles AI-to-AI: how agents coordinate, delegate, and report back. v1.0 shipped March 2026. For most builders today, A2A is background knowledge — your tools will adopt it before you need to implement it.

The token cost section is the most actionable. In a mid-sized stack, MCP tool schemas consumed 66,000–67,000 tokens before the conversation started — roughly a third of Claude Sonnet's context window. Anthropic shipped lazy loading across Chat, Cowork, and Code, so schemas no longer load upfront by default. What still loads: instruction blocks, smaller but real. The fix isn't removing MCPs, it's being deliberate about which ones run in which sessions. The article closes with a three-tier action framework: act now (audit active MCPs, install context-mode), adjust now (tool vs. resource trust evaluation), and background knowledge for later (A2A, MCP Apps).

## Key Sections

- How Did MCP Become the Standard for AI Tools?
- What's the Difference Between MCP, Connectors, Plugins, and MCP Apps?
- What Do MCP Servers Actually Do? The Three Primitives
- Why Are Most MCP Servers Not Worth Installing?
- What Is the A2A Protocol and Do You Need to Care?
- How Much Does Running Too Many MCPs Cost You in Tokens?
- What Should You Actually Do With This Map?
