# Nano Banana 2 in Claude Code: 7 Essential Creator Use Cases

**URL:** https://buildtolaunch.substack.com/p/nano-banana-2-claude-code-deep-dive  
**Published:** March 30, 2026  
**Word count:** ~4,806  
**Engagement:** 29 likes, 2 restacks  
**Access:** Paid

---

## Summary

OpenAI retired the 4o image model that Jenny's hero-image workflow depended on. This article documents a full rebuild of the visual workflow using Nano Banana 2 (Google's `gemini-3.1-flash-image-preview`), tested across 7 creator use cases with 100+ generated images. The article includes real outputs — held-up and broken — alongside the prompt patterns worth keeping and a Claude Code MCP workflow that replaced manual trial-and-error.

---

## What Nano Banana 2 Is

Google's public-facing name for `gemini-3.1-flash-image-preview`, released February 26, 2026. Positioned as the high-efficiency counterpart to Nano Banana Pro: faster, cheaper, built for high-volume generation and conversational editing. Priced to replace workflows that previously required the 4o image model.

---

## The 7 Creator Use Cases

1. **Consistent hero images** — maintaining visual identity across newsletter articles with brand-consistent style
2. **Surface-led text visuals** — images where legible text is part of the composition
3. **Infographics** — structured data visualizations and frameworks as images
4. **Carousel cards** — sequential images for social media content series
5. **Profile rework** — headshots and profile photos with controlled style editing
6. **Targeted image edits** — changing specific elements (background, color, object) without regenerating the full image
7. **Multi-image assembly** — combining outputs from multiple generation passes into one coherent visual

---

## What Held Up and What Didn't

The article includes side-by-side outputs for each use case with verdicts. Nano Banana 2 handled hero images and targeted edits reliably; text legibility was inconsistent in some compositions; multi-image assembly required careful prompting to maintain visual coherence. Prompt patterns that improved reliability across categories are documented.

---

## The Claude Code MCP Workflow

A key efficiency finding: running Nano Banana 2 through a Claude Code MCP setup removes the manual prompt-by-prompt workflow. Once the MCP integration is configured, Claude Code can run batches of image generation tasks programmatically, making large-scale testing and iterative refinement much faster. Setup steps and MCP configuration are included.

---

## Key Sections

1. What Makes Nano Banana 2 Different
2. 7 Use Cases, Real Outputs (preview table)
3. The Deep Dive: Each Use Case Broken Down
4. Run Nano Banana Inside Claude Code (MCP workflow)
