# How I Built a Shared AI Second Brain for Claude, ChatGPT, and Hermes

**URL:** https://buildtolaunch.substack.com/p/shared-ai-memory-second-brain-claude-chatgpt-hermes
**Track:** Hands-on AI Technology
**Published:** 2026-07-27

## Summary

Every AI tool keeps its own instructions, its own skills, and its own memory. Claude Code reads `CLAUDE.md`, Codex reads `AGENTS.md`, Hermes reads its own context files, and each one has separate rules for skill availability, permissions, memory, and scheduled work. The result is that one working preference becomes three instructions, a useful skill exists in one tool and is invisible in the other two, and feedback improves one copy while the rest go stale. Jenny opens on the public evidence that this is not a personal problem: builders describing shared context as a second job, Claude Code fixing a bug that Codex then investigated from zero, months of context lost switching from ChatGPT to Claude. Without a shared layer, the human becomes the synchronization system. Her fix was one maintained file-based second brain that every new AI tool joins with a single instruction: onboard to my AI second brain.

The demonstration is concrete rather than architectural. One skill file lives in one place and appears inside all three tools from each tool's own interface. A correction captured in one tool, once approved, travels with the skill instead of staying local. The same shared layer then carries into real project work, so opening a project from any connected tool produces the same answers cited from the same files. The article ships with the Shared AI Memory Starter Packet, free to paid subscribers, plus a master setup prompt that starts with an included `status-brief` sample skill — proving the route before any existing work moves — and a 10-minute post-setup test with four checks: verify the current skill, propose and record one feedback item, approve one skill revision, and retrieve the current version from a second tool.

The packet's structure follows three terms that keep boundaries clear: canonical source (the authoritative file), executor (the tool or scheduler that runs a job), and approver (the person who authorizes durable changes). `shared-ai-second-brain/` is the common entrance and routing index, holding `START-HERE.md` for humans and `AGENTS.md` for AI tools, plus `SOUL.md` (working preferences), `CHARTER.md` (ownership, privacy, approval rules), `WORKSPACE.md` (routes to projects, skills, connectors, jobs), `STATE.md` (the state of the second brain itself), and a thin `CLAUDE.md` adapter that imports `AGENTS.md`. A routing table decides where anything gets stored: project decisions stay with the project, cross-project knowledge goes to `FOUNDATION/`, reusable procedures go to `SKILLS/`, unowned captures go to `INBOX/`, and addresses go to `WORKSPACE.md`. The rule underneath all of it is one source, never a mirror.

Cross-tool project routing works the same way. Keep one `AGENTS.md` in each project root, which Codex, Cursor, and Hermes read directly, and add a one-line `@AGENTS.md` adapter in `CLAUDE.md` for Claude Code. A project pickup prompt run in fresh tasks across tools should return the same goal, state, latest decision, conventions, and next action, each cited relative to the project root, with native memory and chat history explicitly excluded. A pass is source agreement, not a plausible answer. The skill-improvement loop follows the same discipline: resolve the skill owner, capture feedback without changing the skill, then fold one approved revision into the canonical copy so every tool inherits it.

The piece closes on restraint. It names the security boundary up front — no passwords, tokens, authentication records, raw transcripts, or sensitive third-party information in the shared folder, first run local to one machine, write access granted only when a tool needs to record feedback or apply an approved revision — and it is honest about test coverage, noting the macOS shell installer passed a clean-extraction runtime test while the Windows PowerShell installer passed static safety review with its live runtime test still open. The upgrade section argues against premature tooling: move to Obsidian, Notion, a remote runbook for a cloud scheduler, or a database plus MCP only at a clear limit, not on principle. The file-based layer stays the canonical source until it demonstrably stops working.

## Key Sections

- Why AI Context Drifts Across Tools — separate instruction, skill, memory, and scheduling systems per tool, and the public evidence of the cost
- What It Looks Like With a Shared AI Second Brain — one skill in all three tools, feedback moving with the skill, the layer carrying into project work
- Download the Shared AI Memory Starter Packet — prerequisites, permission boundaries, and what to keep out of the shared folder
- Start Your Shared AI Second Brain With One Prompt — vault, canonical skill, discovery location, pickup prompt, and the master setup prompt
- Run the 10-Minute Post-Setup Test — verify the current skill, record feedback, approve a revision, retrieve the current version
- How the Shared AI Second Brain Packet Is Organized — canonical source / executor / approver, the folder tree, the routing table, and the cold-start sequence
- Route Every AI Tool to the Same Project — one project `AGENTS.md`, the Claude Code adapter, and the project pickup prompt
- Keep One Periodic Job Visible to Every AI Tool
- Improve One Skill From Any AI Tool — resolve the owner, capture without changing, fold one approved revision
- Upgrade Your Shared AI Second Brain Only at a Clear Limit — Obsidian, Notion, remote runbook, database plus MCP
