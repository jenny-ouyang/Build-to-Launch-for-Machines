# How to Onboard to Claude Without the Learning Curve

**URL:** https://buildtolaunch.substack.com/p/claude-onboarding-setup-guide  
**Published:** March 11, 2026  
**Category:** AI Builders Playbook > Tool Setup & Configuration

## Summary

Practical guide for getting Claude to know your work and navigating the full ecosystem (Cowork, commands, skills, plugins, connectors, MCPs) without overwhelming new users. Shows how to onboard teams role-by-role without formal training programs.

## The Baseline Setup (10 minutes, familiar to any AI user)

1. **Desktop app** — claude.com/download (unlocks Cowork features website can't)
2. **Pick the right model** — Sonnet 4.6 (smart enough without Extended Thinking)
3. **Connect your tools** — Settings → Connectors → Google Drive, Gmail, Slack, Notion, etc.
4. **Create a Project and let Memory build** — Organize by work area, Memory learns preferences over time

## Get Claude to Actually Know You (The Breakthrough)

**Instead of telling Claude about your work, show it your work.** Use Cowork (separate tab, works directly with local files).

**Three-step process:**

1. **Let Claude see you** — Point Cowork at 2-3 files representing your actual work. Use this prompt:
   > "Read everything in the shared folder. Look for recurring themes, tasks done manually, frustrations hinted at, goals that never progress, gap between what they say they want and what they do. Produce a personal report: hidden patterns, loops they're stuck in, work done the hard way. Close with one honest observation: the single highest-leverage change."

2. **Let Claude recommend** — After Claude understands your work:
   > "Map what you found directly to Claude's actual features. Be specific. For each capability, write a ready-to-run prompt built around my actual content, not hypothetical. End with ranked list: the three Claude capabilities with highest impact on my work, and why."

3. **If too many files** — Use three-pass approach: Map (inventory), Select (pick 5-7 most revealing), Reflect (produce personal report)

## The Ecosystem Explained (One Walkthrough: Substack Notes)

**The layers stack — you use whichever fits the moment:**

1. **Chatbox** — Basic conversation. Type, Claude responds. Every AI works this way. Generic output.
2. **Cowork** — Points at folder on your computer, reads past notes, knows your voice/format.
3. **Slash command** — Shortcuts for repeated prompts (`/draft-notes`, `/schedule-notes`).
4. **Skill** — Domain expertise that activates automatically (makes formula/spacing decisions).
5. **Connector/MCP** — Bridge to external tools (Substack API, schedules directly).
6. **Plugin** — Everything bundled together (skill + commands + connector in one package).

**Key insight:** You're not choosing one layer. You're choosing the right layer for the task at hand. Automated workflow vs manual control.

## Your First Plugin & Command (By Role)

**11 official Anthropic plugins mapped to jobs:**

- **HR:** onboarding plans, offer letters, policy summaries
- **Finance:** journal entries, variance analysis, reconciliation
- **Marketing:** content calendars, campaign briefs, brand guidelines
- **Sales:** call summaries, forecast updates, outreach templates
- **Operations:** process docs, vendor review, status reports
- **Everyone:** meeting summaries, email drafts, research synthesis

**First command to try:** Start with one domain-specific task, not a generic "help me with X."

## Claude Code vs Desktop

**Desktop (Cowork):** App-based, reads files, creates docs/spreadsheets/presentations. Context window compacting on Pro tier ($20/month) when using many plugins.

**Code:** Lives in terminal, reads entire codebase, writes/tests/deploys software. Smoother than Cowork (no context limits, no plugin caps) but requires CLI comfort. Best for actual software development.

## Rolling This Out to a Team

**Don't onboard everyone at once.** Pattern:

1. Pick one champion per role → give them 20 min with this guide
2. Let them use it for a week on real work
3. They demo to their team using actual company files (not hypothetical examples)
4. Expand role by role

**Key:** Champions show, not tell. Real files, real workflows, real results.

## Gifts Included

1. **Substack Notes Plugin** (paid members) — drafts/schedules notes via slash commands + 7 formulas + MCP
2. **Official Claude Plugins** (free gift for everyone) — all 11 Anthropic plugins in .md format to adapt for free Claude or any AI

## Core Philosophy

**Instead of explaining workflows to Claude, show Claude your work.** The shift from "tell" to "point at files" is what unlocks personalized AI without 20-question sessions. Quality isn't prompt-based. It's context-based.
