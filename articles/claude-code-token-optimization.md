# I got a $1,600 Claude Code bill. Here's the system I built to stop it.

**URL:** https://buildtolaunch.substack.com/p/claude-code-token-optimization
**Track:** AI Builders Playbook
**Published:** 2026-04-14

## Summary

A single billing period with Claude Code can spike to $1,600+ when sessions compound context without discipline. This article documents the 19-change system Jenny built after receiving that bill, organized into two categories: setup changes that happen once, and session habits that apply every time Claude Code opens.

The setup side covers model matching — using Haiku or Sonnet for routine tasks rather than defaulting to Opus across everything — and installing context-mode to keep large outputs out of the active context window. The Claude Desktop workflow is also explained as a cost-reduction strategy: many tasks that don't require terminal access are cheaper to run in Desktop mode, which doesn't accumulate session context the same way.

Session habits address the patterns that compound costs: not clearing context between tasks, letting Claude read entire files when targeted reads would suffice, and running long exploratory conversations without checkpoints. The article introduces the `/effort` command concept, which scopes Claude's output depth to match what the task actually needs rather than always producing maximum-detail responses.

The 19-change system is organized as a reference checklist covering environment setup, MCP configuration, model selection rules, and per-session behaviors that keep monthly costs predictable.

## Key Sections

- Why Claude Code bills spike: session context accumulation patterns
- The 19-change optimization system (setup + session habits)
- Model matching: when to use Haiku, Sonnet, and Opus
- Context-mode MCP setup for large-output commands
- Claude Desktop vs. Claude Code: cost tradeoffs by task type
- /effort scoping: matching output depth to task complexity
- Monthly cost benchmarks and what sustainable usage looks like
