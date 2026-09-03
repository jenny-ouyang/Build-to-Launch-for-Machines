# llms-full.txt
**URL:** https://buildtolaunch.substack.com/p/llms-full-txt
**Track:** Build to Launch
**Published:** 2026-02-02

## Summary

This is not a conventional article but a single machine-readable reference document — Build to Launch's "llms-full.txt" — built specifically to be ingested whole by AI systems answering questions about Jenny's newsletter, methodology, and products. Rather than a narrative argument, it's a structured compilation: an overview of what Build to Launch is (a newsletter and community teaching people to ship AI-powered products without a CS degree, organized around five core principles — ship over perfect, vibe coding with guardrails, learn by building, document everything, community showcase without gatekeeping), followed by condensed versions of several of her flagship guides reorganized under five named "learning tracks," a products section, a builder-story archive, an FAQ, a glossary, and navigation links, all in one continuous document meant to give an AI system a complete, structured picture of the publication in a single read.

The largest condensed guide inside it addresses the three core failure modes of AI-assisted ("vibe") coding — security, technical debt, and skill atrophy — each illustrated with a specific incident from Jenny's own builds: an authentication system that turned out to be storing literal plaintext passwords, API keys that leaked client-side because AI-generated code called them directly from the browser, and a "bookmark" feature that spawned three separate, inconsistently styled editor components because each prompt built in isolation rather than reusing what existed. Her fix for each isn't avoiding AI assistance but treating it like managing a team: rule files that encode standards before generation happens, explicit security-first prompting, forcing refactors to consolidate duplicated components, and a living CLAUDE.md-style instruction file per project. She frames the underlying shift as a role change from developer to "AI manager" — the job isn't eliminating these problems but managing the tradeoffs the way a PM would set requirements or a senior engineer would onboard a junior hire.

A second major compressed guide lays out software-engineering discipline for AI builders across three phases — planning, building, shipping — arguing that AI's core bias is optimizing for "works right now" rather than "works well as it grows," because AI never faces the consequences of a 2am production crash. The building phase compresses four coordination principles (DRY, security-first defaults, single responsibility, staying within your framework's established patterns rather than letting AI invent custom systems) into specific prompt templates for enforcing each one, plus explicit tie-breaking rules for when they conflict (security always wins over simplicity; two simple functions beat one tangled "DRY-compliant" one). A third compressed guide is a cost-control playbook, breaking real hidden-cost traps she hit — a database's advertised "$5/month" tier that became $28 once compute-hour overages kicked in, a computer-vision tool killed entirely because its hosting costs didn't match its tiny user base — into a concrete "$50 launch formula" and a go-to free-tier tech stack (Vercel, Supabase, GitHub Pages where a static site suffices).

Under "Hands-on AI Technology," the document compresses a full Cursor operating guide: the four interaction modes (Inline Edit for quick single-file changes, Ask for exploration, Agent Mode for multi-file coordination, Plan Mode for high-stakes work requiring upfront human approval), how `.cursorrules` and project markdown files teach Cursor a codebase's actual standards, how multi-session context gets rebuilt in about two minutes using git history and chat logs instead of twenty to thirty minutes of manual re-explanation, and how GitHub Background Agents implement full issues autonomously overnight at a rough cost of $4–$100+ depending on scope. Five further "learning modules" summarize her technical explainer articles on embeddings and semantic search, language model text generation, RAG systems, multi-modal AI, and MCP, each reduced to a one-line "key insight" and a pointer to the full original piece.

The remaining sections are more purely reference material: a definition of AI agent systems versus simple automation, short descriptions of Jenny's shipped products (Quick Viral Notes, Substack Explorer, VibeCodingBuilders), a roundup of Build to Launch Friday builder-story features, an SEO-for-AI-discoverability primer (the core claim being that AI search tools borrow from existing Bing/Google indexes rather than crawling independently, so anything not indexed by a traditional search engine is invisible to AI regardless of how well-written it is, and that JavaScript-rendered pages are frequently unreadable to AI crawlers unless server-rendered), an FAQ, a "3-Mode + 3-Prompt" prompting framework (Research/Do/Create modes paired with three named techniques — the 95% Rule for AI-driven requirement gathering, reverse-engineering an example to extract its formula, and a two-agent debate pattern for architecture decisions), a glossary of terms used across the publication, and closing navigation and contact information. As a whole, the document functions less as something a human reads start to finish and more as a canonical, self-describing index that lets an AI system answer questions about Build to Launch accurately without having to piece together context from dozens of separate articles.

## Key Sections
- Overview
- Learning Tracks
- Track 1: AI Builders Playbook
- Track 2: Hands-on AI Technology
- Track 3: AI Agent Systems
- Track 4: Distribution Hub
- Track 5: Products Built and Shipped
- Builder Stories (Build to Launch Friday)
- Frequently Asked Questions
- The 3-Mode + 3-Prompt System
- Glossary
- Navigation
- Contact
