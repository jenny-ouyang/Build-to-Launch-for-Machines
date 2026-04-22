# MCP, Plugins, and Skills — How to Know Which One to Reach For

**URL:** https://buildtolaunch.substack.com/p/claude-code-mcp-vs-plugins-vs-skills
**Track:** AI Builders Playbook
**Published:** 2026-04-11

## Summary

Anthropic shipped three extension layers for Claude Code in under a year — MCP (November 2024), Plugins (October 2025), and Skills (October 2025) — and the community installed all three without getting clear on what each is actually for. The confusion has a specific cause: most builders treat plugins as a third category alongside skills and MCP, when plugins are actually bundles of the other two. This article settles that framing and maps out when to reach for each layer.

Skills are the lightest layer: markdown files that tell Claude how to handle a specific task, invoked with a slash command, costing around 30-50 tokens per skill and only when active. They're for encoding repeated workflows — code review against your standards, content drafts in your format, incident write-ups. The failure mode is overstuffing: two skills that say almost the same thing, or one skill trying to do a job that needs live external data.

MCP servers are the opposite: expensive upfront (a typical five-server setup uses approximately 55,000 tokens before any conversation starts), but the only way to give Claude real reach — live databases, APIs, files, email, GitHub. The article covers when MCP is overkill (encoding a workflow or process belongs in a skill, not MCP), the Anthropic Tool Search feature that reduces the upfront cost by 85%, and a real example: a four-Gmail-account setup that produces a 40-second morning brief across all four accounts.

Plugins package the other two layers for reuse or sharing: a working combination of skills, hooks, and MCP configs bundled so it can be installed in one step or deployed across multiple repos. The article covers what's actually inside a plugin bundle (hooks are the automation glue that fire on events and make plugins feel automatic), tested 11 plugins on real work, and gives a clear rule for when a plugin is worth installing versus when you could write the same thing yourself in 30 minutes.

The final section shows how all three work together in a live stack: a skill holds the logic, an MCP server provides the data access, and an automation layer (OpenClaw in this case) runs it on schedule. The recommended build order is always skill first, then MCP when the skill hits a data wall, then plugin when reusability becomes the actual problem.

## Key Sections

- MCP vs Skills vs Plugins: what each layer actually does — three problems, three tools
- What are Claude Code Skills and when should you use them? — 30-50 token cost, failure modes
- When to use MCP in Claude Code (and when it's overkill) — 55,000-token upfront cost, scoping rules
- What are Claude Code Plugins? (they're not a fourth category) — bundle anatomy, hooks explained
- MCP vs Skills vs Plugins: which one to use for each job — decision flowchart
- How MCP, Skills, and Plugins work together in one stack — build order and real GSC automation example
- How to start: the right order for your Claude Code setup
