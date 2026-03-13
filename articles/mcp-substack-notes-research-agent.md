# I built an AI research tool to study Substack creators I admire. Here's what 3,000 notes show.

**URL:** https://buildtolaunch.substack.com/p/mcp-substack-notes-research-agent  
**Published:** March 13, 2026  
**Category:** Hands-on AI Technology > AI Research & Domain-Specific Agents

## Summary

Jenny built a custom MCP (Model Context Protocol) server to analyze 3,230 Substack notes from 9 AI/tech creators at scale, revealing data-backed patterns that contradict conventional advice. The research shows that post-link notes (the most-posted format) are the worst performers, while pure text tactical revelations consistently drive the highest engagement.

## Key Findings

**Five patterns that held across all nine creators:**

1. **Pure text outperforms everything** — Top performers post 70%+ pure text. The catch: consistency matters more than format.
2. **Post-link notes underperform** — Most-posted format, worst results. Exception: when the body is complete without clicking.
3. **Highest-comment notes ≠ most useful** — Notes that name behaviors people don't admit out loud generate conversation. Notes that teach generate likes.
4. **Volume alone doesn't explain performance** — Three creators with 475-499 notes had per-note averages of 8.7, 33.5, and 37.7 (4x gap). Worldview coherence beats volume.
5. **One viral note raises your floor once, consistent voice raises it permanently** — 33-average across 499 notes compounds far beyond a single spike.

## Five Note Types Worth Writing

1. **The Tactical Revelation** — Specific claim + immediately usable thing in the note body. Complete without clicking. (e.g., "My prompt quality skyrocketed when I added one phrase..." — 1,891 likes)
2. **The Named Behavior** — Names something people do but don't admit. First person. No solution at the end.
3. **The Worldview Statement** — Clear take, no hedge. Not tips, just what you actually think.
4. **The Milestone Done Right** — Personal update + specific transferable detail readers can take with them.
5. **The Post Link Done Right** — Note body is complete, linked article is optional depth.

## Research Methodology

Built a custom MCP that fetches up to 500 recent notes per creator with full metadata (body text, likes, comments, restacks, attachment type). Three-pass analysis in Claude:

1. **Pass 1:** Classify by attachment type, sort by likes, pull top 10 per creator
2. **Pass 2:** Identify structural patterns across top performers (not topics, structure)
3. **Pass 3:** Surface patterns that hold across all nine, not just one creator

Total data: 4,100 items fetched, 3,230 clean notes after filtering out noise. Nine creators: Wyndo, Mia Kiraki, Sam Illingworth, James Presbitero, Anfernee, Karen Spinner, Orel Tajar, Code Like A Girl, Jenny Ouyang.

## How to Run Your Own Version

**Three-pass framework (manual, ~20 min):**

1. **Format-engagement gap** — Classify last 30 notes by type, calculate average likes per format
2. **Go structural** — Pull top 5 notes, answer: specific claim or vague? Value in note or behind click? Names behavior or tells what to do?
3. **Find contradictions** — Where does data show something different from what you thought you were doing?

**At scale:** Use the Substack Research Plugin (included in paid membership) or join office hours for guided setup.

## Key Insight

**Context beats prompts.** The Voice Extraction prompt works because it analyzes 5 real articles and produces a portable artifact (Voice Card) that persists across sessions. The Workflow Orchestrator prompt works because it collapses a 7-step multi-tool workflow into one command with quality gates. AI research isn't just for building apps — it's how to surface patterns human scrolling can't see.
