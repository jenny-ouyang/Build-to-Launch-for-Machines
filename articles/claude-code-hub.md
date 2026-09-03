# Claude Code Hub
**URL:** https://buildtolaunch.substack.com/p/claude-code-hub
**Track:** AI Builders Playbook
**Published:** 2026-02-20

## Summary

This is a living index page rather than a single narrative article: a hub that organizes every Claude and Claude Code guide Jenny has published — 35+ by the article's own count, grown from three since early 2025 — by the question a reader is actually trying to answer rather than by publish date. The framing device is personal and specific: a year of daily use, including a $1,600 monthly bill she didn't see coming before she diagnosed what was compounding it, sits behind the hub's existence. She positions it as the resource she wishes had existed when she started, and structures it as a path to walk in order for newcomers (What is Claude → install → first project → prompts and subagents → cost control → MCP → plugins/skills/modes → production → compare alternatives) while also functioning as a jump-to reference for people who already know what they're looking for.

The hub opens by naming a confusion it says drives most frustration: "Claude" actually covers three separate products — Claude the chat interface, Claude Code the terminal-based coding agent, and Claude Cowork, which handles scheduled routines and background automation — and most guides elsewhere conflate them. From there the hub organizes its links into topic sections. "Understanding Claude" separates the three products and compares Claude's extension model (MCP, plugins, skills) against ChatGPT's Custom GPTs and Gemini's Gems. "Install & First Project" covers a from-scratch install aimed at non-developers and a structured onboarding pass for teaching Claude a reader's actual files and project context, which the hub argues most builders skip, then spend weeks fighting a Claude that doesn't understand their project. "What to Build" reframes the usual "what app should I build" question into "what daily problem can I solve today," pointing to a 15-project tier list (local/reversible, connected/stateful, autonomous/scheduled) and a 70-minute app-idea validation workflow that researched 16 competitor sites using parallel agents before a real launch.

"Better Results" gathers the prompt-craft and reasoning-pattern guides: a curated set of 15 daily-use prompts, a setup for turning named creators into on-demand AI mentors, a prompt that reverse-engineers a creator's business model, the research framework covered in a separate live-session article, prompting principles that transfer across AI coding tools generally, an explainer on subagents (and the specific claim that a subagent's description field, not its capability, is what determines whether Claude routes work to it correctly), and a dynamic-workflows piece about spawning up to 100 parallel agents in one session that fact-check each other before merging a result. "Cost Control" links back to the $1,600-bill story directly, breaking 19 fixes into setup changes, session habits, and project patterns, alongside a local-model (Ollama) setup for cutting API costs to zero on workflows that don't need frontier models.

The largest section by volume is "MCP & Connections," running from a concept-level explainer of what MCP unlocks through a map of the confusing apps/connectors/plugins ecosystem, a guide to the different MCP server types (stdio, HTTP, OAuth) and their distinct failure modes, a ranked list of 16 servers by actual daily utility, a pay-per-result MCP (Apify) that can also generate income by publishing your own actors, cross-client setup spanning Claude, ChatGPT, VS Code, and Cursor, several NotebookLM-paired research workflows, a multi-account Gmail setup, and a from-scratch MCP server build guide. "Plugins, Skills & Modes" collects tested verdicts rather than feature descriptions — 11 plugins tested with 4 worth keeping, a debugging guide built from auditing 20+ non-triggering skills, an 18-task honest breakdown of Claude's five remote modes, and separate coverage of Chrome browser automation, image generation (Nano Banana), routines, and scheduling. "Production" and "Compare Tools" round it out with the discipline needed to take a vibe-coded project live and head-to-head comparisons against Cursor and other AI coding tools, plus a four-level framework for choosing between Claude-native automation, n8n, and OpenClaw by task complexity.

A "Claude Updates 2026" section functions as a changelog layer on top of the topic index, tracking how Claude "unbundled" through the year into distinct surfaces (Chat, Cowork, Code, Design) each with different permissions and cost structures — the hub's argument is that choosing the wrong surface, not prompting skill, became the most common reason workflows failed once the product fragmented this way. A closing FAQ answers the most basic framing questions directly: what Claude Code is (a terminal agent with direct filesystem access, distinct from both Claude chat and GitHub Copilot), whether non-developers need it (no, but terminal comfort helps), how it differs from Cursor (an agent you hand tasks to versus an IDE you write inside), what it actually costs per token, and what CLAUDE.md is for (a standing project-context file Claude reads at the start of every session).

## Key Sections
- Understanding Claude
- Install & First Project
- What to Build
- Better Results
- Cost Control
- MCP & Connections
- Plugins, Skills & Modes
- Production
- Compare Tools
- Claude Updates 2026
- FAQ
- The path through this hub
