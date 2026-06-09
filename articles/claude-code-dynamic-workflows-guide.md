# Claude Code Dynamic Workflows: How 100 Agents Research, Write, and Build in One Session

**URL:** https://buildtolaunch.substack.com/p/claude-code-dynamic-workflows-guide
**Track:** AI Agent Systems
**Published:** 2026-06-03

## Summary

Claude ships features faster than anyone can track — Skills, MCP servers, plugins, connectors, Cowork, Routines, model upgrades all inside eight months — and most people stop looking. Dynamic workflows is the one that caught Jenny off guard. She asked Claude to research MCP servers on a normal Tuesday and it quietly spun up 101 agents, ran them for 13 minutes across 723 searches and page-reads, and only then handed back an answer. Seventy-five of those agents were fact-checking, each trying to prove a finding wrong. That wasn't her usual workflow, so she stopped the research and took the feature apart instead.

A dynamic workflow turns one request into many agents working in parallel, with the results checked before they reach you. You describe the task; Claude writes a small program that breaks the work into pieces, runs many copies of itself on those pieces at the same time, and merges what comes back. In this case Claude reached for a built-in workflow called deep-research entirely on its own. The article walks through what the program actually did, what roles the hundred agents played, and why a verification-heavy fan-out changes the trust you can place in an AI's output — most of the agent budget went to refuting findings, not generating them.

The middle of the piece moves from observation to reproduction. It explains how a dynamic workflow is built — the Workflow Designer that authors the orchestration program — and then gives three copyable recipes plus three ways to run any recipe, so the same fan-out-and-verify pattern works whether or not you have the built-in feature. The point is that the structure (decompose, run in parallel, verify adversarially, synthesize) is portable to any AI tool, not locked to Claude Code's binary.

It closes with judgment: when a dynamic workflow is worth the tokens versus when it's overkill, since spinning up a hundred agents for a simple question wastes both time and money. There's also a "one more thing I found in the binary" section surfacing a detail pulled from inspecting Claude Code directly, and a Next Steps block with concrete actions to try the pattern on your own research, writing, or analysis today.

## Key Sections

- What dynamic workflows are in Claude Code
- What 100 agents do in one workflow run
- Why dynamic workflows change how you work with AI
- How a dynamic workflow is built (the Workflow Designer)
- What I actually ran, and what came back
- How to build your own workflow without the feature (three recipes, three ways to run any recipe)
- When a dynamic workflow is worth the tokens
- One more thing I found in the binary
- Next Steps / What you can do today
