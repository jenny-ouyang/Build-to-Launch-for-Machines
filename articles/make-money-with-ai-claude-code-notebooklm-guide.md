# How to Make Money With AI: From Research to Act in One Loop

**URL:** https://buildtolaunch.substack.com/p/make-money-with-ai-claude-code-notebooklm-guide
**Track:** Hands-on AI Technology
**Published:** 2026-05-09

## Summary

Most people trying to make money with AI are stuck collecting — playbooks, creator strategies, income models — and never converting any of it into a decision, a product, or a system. AI has only accelerated the collecting. The article names the exact failure point: research results come back, they get read once, and then the tab closes. That is not a motivation problem; it is a routing problem. Research needs a destination.

The piece lays out three routes for research output. **Route 1: Learn and collect** is for mapping a space you don't yet understand. **Route 2: Make a decision** is for committing to a path once you have enough signal. **Route 3: Track and monitor** is the route most people skip and the one with the strongest income connection — building a system that keeps you current on a space where the best operators keep shifting their approach. The live build in this session targets Route 3.

Before the build, the article catalogs the six current ways people make money with AI: content creation (audience-based revenue), knowledge selling (courses and cohorts), services and consulting, productized workflows, AI systems (build-and-license), and community access. Most serious players run more than one. The session focuses on content creation and knowledge selling, using Alex Hormozi as the demo subject because his work is dense, framework-heavy, and publicly available.

The full live build connects four tools into a single loop. **Perplexity MCP** retrieves the top creators in a target space and pulls their YouTube content. **NotebookLM MCP** stores that content and runs three structured query batches against it — Batch 1 (15 core-belief questions), Batch 2 (45 mechanics-and-frameworks questions), and Batch 3 (~40 failure-mode questions) — producing a structured export of the creator's beliefs, frameworks, field crimes, personality model, and system design logic. The example query "How would Alex Hormozi criticize the Practical AI Builder Program's marketing?" returns a pointed critique grounded in his actual stated frameworks, not generic advice.

The mentor is a snapshot, so the next layer is a **tracking skill** that auto-swaps the oldest source in the notebook for the creator's newest YouTube content. Claude builds the skill live in the session and saves it to the **Build to Launch MCP** so it can be called from anywhere. Connected to a **Claude scheduled task** running weekly, the skill turns the mentor from a workflow (runs when you start it) into an autonomous system (runs on its own). The final loop: Perplexity finds the creators → Perplexity pulls their content → NotebookLM builds the mentor → you apply the mentor to your own work → the tracking skill keeps the notebook current → the scheduled task runs the skill on cadence.

The session closes with two questions from the group. **Where do outputs land?** By default, Build to Launch skills write to a dated file in `Documents/Build-to-Launch-Outputs`, but the path can be redirected to Obsidian, Notion, GitHub, or anywhere else durable. **Can this become a paid product?** Yes — the Gumroad prompt collections came out of exactly this kind of internal-tool-turned-package. The system you build for yourself is often the product. The piece ends with a three-step homework: name your income output, take one step, drop it in the Substack chat.

## Key Sections

- What the real bottleneck is after you get research results back
- 3 routes for turning research results into action
- 6 ways people make money with AI
- How to retrieve the best research output (Perplexity)
- How to hire your digital mentor (NotebookLM with 3 query batches)
- How to build your tracking skill (auto-swap oldest source for newest content)
- How to build your autonomous system (skill plus scheduled task)
- The complete loop connecting all 4 tools (Perplexity, NotebookLM, Build to Launch MCP, Claude)
- Live updates from the session and audience Q&A
- Session timeline with timestamps
