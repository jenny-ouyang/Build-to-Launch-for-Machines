# Claude Cowork Scheduled Tasks vs Local Routines vs /loop vs Cloud Routines: What's Actually Different (2026)

**URL:** https://buildtolaunch.substack.com/p/claude-cowork-scheduled-tasks-vs-routines-vs-loop
**Track:** AI Agent Systems
**Published:** 2026-05-03

## Summary

Anthropic shipped most of these in the same year and never drew the product map. This article maps Claude's five surfaces and four native scheduling modes, then gives you one question that routes every automation job to the right tool.

The five surfaces: claude.ai web (conversational, no automation), Claude Cowork inside Desktop (the non-developer automation layer with Scheduled Tasks), Claude Code CLI (terminal-native, where /loop lives), Claude Code Desktop (the redesigned April 2026 GUI with the Routines tab), and Claude Dispatch (a remote trigger bridge, not an automation tool — execution still happens locally). Cowork and Claude Code share the same Desktop app but are distinct product layers.

The four scheduling modes: /loop is session-scoped, dies when you close the terminal, auto-expires after three days. Cowork Scheduled Tasks are the non-developer entry to Desktop's local scheduling engine. Local Routines are the developer-facing entry to that same engine — same runtime behavior, different interface and persona. Cloud Routines run on Anthropic's infrastructure independent of your machine. The Cowork/Local Routine confusion is real because they look like siblings but route to different users; the article makes the distinction explicit. What kills each: /loop dies on terminal close or sleep. Local Routines and Cowork Scheduled Tasks miss runs when the app is closed (one catch-up fires on wake). Cloud Routines fail when tasks need uncommitted local files, local MCPs, or persistent state.

The routing rule is one question: what happens if this run fails? Tier 1 low risk (missing report, blank digest) — any Claude-native tool works. Tier 2 medium risk (wrong data written, workflow stalls) — use Routines or Scheduled Tasks but build in a review step. Tier 3 high risk (wrong email, deletion, live publish, charge triggered) — don't use a single-layer Claude tool, you need n8n with approval loops. The automation tool isn't the decision. The failure cost is.

The article closes with the author's actual stack split. About 80% of OpenClaw workflows moved to Cloud Routines after the April 2026 redesign — weekly research digest, daily inbox triage, GSC opportunity review, social notes pipeline, doc sync. /loop runs active error monitoring during coding sessions. Local Routines handle Substack notes scheduling because it needs local MCP access. The remaining 20% stayed in OpenClaw because they need persistent memory across runs or full file system access — capabilities Routines don't provide. n8n covers the deterministic, integration-heavy jobs touching payments, CRMs, or production databases. A five-question decision flow at the end routes any new job: machine off, local files, persistent memory, external systems, failure cost.

## Key Sections

- What's in Claude's Complete Ecosystem? (the five surfaces)
- Claude's Four Scheduling Modes: Which One Is Right for You?
- What kills each one (/loop, Cowork Scheduled Tasks, Local Routines, Cloud Routines)
- The same task run four ways
- The One Question That Routes Every Automation Job (3-tier failure cost framework)
- When Claude's Native Tools Reach Their Ceiling (memory + determinism)
- My Actual Automation Stack: Which Jobs Live Where
- How to Decide Where Each Claude Automation Lives (5-question flowchart)
- Frequently Asked Questions
