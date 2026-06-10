# What Are Claude Code Subagents? (And How to Make the Most of Them)

**URL:** https://buildtolaunch.substack.com/p/claude-code-subagents-explained
**Track:** AI Agent Systems
**Published:** 2025-12-22

## Summary

Claude Code subagents are separate Claude instances that run research, analysis, or tasks in parallel, each in its own context window, while the main conversation stays clean. The article's central surprise is that most builders already have three built-in subagents waiting in Claude Code without any setup. It covers what subagents are, which ones you already have, when to spawn them, when to skip them, and what breaks when the decision goes wrong.

It opens with how subagents actually work — why a separate context window matters, and how delegating to one keeps the main thread from filling up with intermediate results. Then it names the built-in subagents the reader already has, so the first win requires no configuration at all.

The decision content is the core: parallel versus sequential subagents and when each is the right call. Parallel fans out independent work; sequential chains steps that depend on each other. The article maps real, no-code uses for subagents so a non-developer can see where they help, then gives a five-minute walkthrough for creating a custom subagent.

The back half is about not getting burned. It documents five failure modes and their fixes, provides starter configs to copy, and lays out how to get started today. The throughline is that subagents are a force multiplier only when the work is genuinely separable — used on the wrong task, they add overhead and muddy results rather than speeding anything up.

## Key Sections

- How Claude Code Subagents Work
- Built-In Claude Code Subagents: What You Already Have
- Parallel vs. Sequential Subagents: When to Use Each
- What Can You Use Claude Code Subagents For? (No Code Required)
- How to Create a Claude Code Subagent in 5 Minutes
- Claude Code Subagent Troubleshooting: 5 Failure Modes and Fixes
- Claude Code Subagent Starter Configs
- How to Get Started With Claude Code Subagents Today
