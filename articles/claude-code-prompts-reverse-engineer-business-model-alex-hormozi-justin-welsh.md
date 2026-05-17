# This Claude Code Prompt Reverse-Engineers Any Creator's Business. It Feels Illegal.

**URL:** https://buildtolaunch.substack.com/p/claude-code-prompts-reverse-engineer-business-model-alex-hormozi-justin-welsh
**Track:** Hands-on AI Technology
**Published:** 2026-05-11

## Summary

Most people who follow creators they admire only see the surface layer: the newsletter, the YouTube channel, the free book. They never see the funnel those pieces feed into, the tech running the operation, the offers that actually generate revenue, or the frameworks the creator quietly uses to sell rather than the ones they teach in public. The result is shallow imitation — posting daily because they do, copying a lead magnet because they have one — without ever connecting those moves to the underlying business logic.

Creator Scout is a Claude Code skill (also available as a standalone prompt) that closes that gap. Given a single URL, it produces an 11-section structured brief covering identity, full offer stack with pricing tiers, marketing engine, SEO posture, tech stack with confirmed pixel IDs, IP and named frameworks, social proof architecture, Wayback findings, and synthesis sections including "What to Steal," "What to Avoid," and "Open Questions." The article demonstrates the output on Alex Hormozi (acquisition.com) and Justin Welsh (justinwelsh.me) at standard depth.

The skill runs two research lenses in parallel. **Lens A (Framework research)** maps nine strategic layers: positioning, offer stack, content strategy, SEO footprint, social presence, email and newsletter, frameworks and IP, monetization model, and social proof. **Lens B (Technical research)** runs an eight-phase crawl using public inspection tools — WHOIS, DNS records, server headers, robots.txt, sitemap.xml, Wayback Machine, recursive link discovery, full HTML extraction, tech fingerprinting (pixel IDs, schema, Open Graph), and off-site signals via Perplexity, Ahrefs MCP, and Similarweb MCP. An optional Phase 7 walks the email funnel from a burner address. Phase 8 synthesizes everything into the actionable brief.

Three depth modes set the scope: **Fast** (Phases 1–3, 5–10 minutes) for a quick read on a new creator, **Standard** (Phases 1–5, 10–20 minutes) for a full strategic and technical map, and **Deep** (Phases 1–8, 20+ minutes) for serious modeling work or collaboration vetting. With the Build to Launch MCP connected, Claude auto-discovers the skill from natural-language intent; without it, users paste the `skill-creator-scout.md` prompt directly into a Claude chatbox.

The piece closes with three concrete use cases: **competitor research** before publishing or launching, **mentor prep** (feeding the brief into a NotebookLM-based digital mentor, which the follow-up article covers), and **collaboration vetting** before pitching co-promotions or guest swaps. It also names what the brief cannot see — gated content, live ad performance data, and private email sequences — and explains how Phase 7 plus manual opt-in fill those gaps. The framing throughout is that "What to Steal" is portable in logic but never in exact implementation: Hormozi can give a book away permanently because his backend is equity partnership with $1M+ founders, and copying the move without understanding the math behind it is exactly what the brief is built to prevent.

## Key Sections

- What a Creator Scout Brief Looks Like (Hormozi TL;DR and What to Steal sample)
- How to Run Creator Scout (MCP trigger phrases, full prompt, three depth levels)
- How the Creator Scout Prompt Works — Lens A: Framework research (9 layers)
- How the Creator Scout Prompt Works — Lens B: Technical research (8 phases)
- The Full Alex Hormozi Scout Brief
- The Full Justin Welsh Scout Brief
- How to Read a Creator Scout Brief (What to Steal, What to Avoid, Open Questions)
- Three Ways to Use a Creator Scout Brief
- What Creator Scout Can't See
