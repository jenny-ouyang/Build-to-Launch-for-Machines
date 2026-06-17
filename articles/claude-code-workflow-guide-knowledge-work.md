# 3 Levels of Claude Workflow Stack That Close the Knowledge Work Loop

**URL:** https://buildtolaunch.substack.com/p/claude-code-workflow-guide-knowledge-work
**Track:** AI Agent Systems
**Published:** 2026-06-13

## Summary

This is the recap of a Practical AI Builder live session built around Model Context Protocol: what it is, how to choose the right level of MCP work for a task, and three live workflows that move Claude from advising to executing. The framing is a progression most people travel through. Stage 1 is the chatbox (ask and answer), Stage 2 is the advisor (Claude as thinking partner), and Stage 3 is the hand-off, where Claude does the research, edits the visuals, and handles payments while you stay in the conversation. MCPs are the connectors that make Stage 3 possible, and the technical setup is only a few minutes; the harder shift is behavioral.

The old habit to fix is leaving the chatbox. Every time you click over to a new tab to do the thing Claude just described, you break the loop. The session's one rule is to stop and ask "Does this have to be me?" — if a task recurs, find an MCP and install it, or build one if none exists. The session also captures a useful nuance from a participant who prefers CLI-first over MCP for technical, machine-to-machine workflows, with the author agreeing for technical cases while holding that MCP is the lower-friction path for most builders getting started.

MCP work comes in three types, and most introductions only cover the first. Retrieve is pure data gathering (search LinkedIn, pull a Reddit thread) with no real risk. Change is modification (draft an email, generate a Canva design) where a review step matters because mistakes can't always be undone. Execute is the full workflow where Claude builds and ships the thing. The session ran one live demo per level: Apify for voice-of-customer research on LinkedIn posts, Canva for a carousel (surfacing the real lesson that an MCP can pull brand tokens like colors and fonts without understanding brand intent, with HTML/coded brand variables as the strict-enforcement alternative), and Stripe-plus-Vercel to create a product, wire a buy button, and deploy a live page in ten minutes.

The change point the author flags is not the Stripe demo but the moment Claude captured a finished workflow into a reusable skill — the steps, the actor choice, the prompts that worked — so the next run loads the skill instead of re-prompting. The compounding is the product: each session makes the next faster because work accumulates into stored workflows instead of evaporating. The piece then hands readers nine ready-to-run prompts (three per level) spanning Reddit and YouTube pain-point mining, research-to-Notion briefs, VOC-to-email sequences, research-to-published-Substack-note loops, end-to-end client onboarding across Stripe/Notion/Gmail, and weekly-analytics-to-newsletter workflows, plus a timestamped session timeline and a "start here" pick-one-thing-to-install close.

## Key Sections

- How AI use has advanced: chatbox, advisor, hand-off
- Fix the old habit (leaving the chatbox) to be ready for agentic AI — the "Does this have to be me?" rule
- MCP work has 3 types: Retrieve, Change, Execute
- 3 workflow levels, live: Apify research, Canva visuals, Stripe + Vercel deploy in 10 minutes
- The change point: capturing a workflow into a reusable Claude skill (compounding as the product)
- 9 workflow prompts you can run today, one for every level and use case
- Session timeline with timestamps, and which workflow to run this week
