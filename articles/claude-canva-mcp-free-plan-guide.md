# Claude + Canva MCP: Make Repeatable On-Brand Designs on a Free Plan

**URL:** https://buildtolaunch.substack.com/p/claude-canva-mcp-free-plan-guide
**Track:** AI Agent Systems
**Published:** 2026-06-24

## Summary

The Canva MCP is a connector that lets Claude operate a Canva account directly, building designs and handing them back as real, editable files (PNG, PDF, full slide decks) rather than flat AI images with text baked into the pixels. The setup is two free steps: register on Canva and add the connector in Claude (or any assistant that supports connectors). The headline finding is that a free Canva plan produces the whole kit, from one article Claude generated an infographic, a 9:16 story, an Instagram square, a YouTube thumbnail, and a seven-slide carousel, each arriving as an editable Canva design. Canva's own AI tools cap at ten lifetime generations, but the import path has no cap because Claude builds the design as HTML and imports it, spending no Canva AI credits.

The reusable layer is a skill. On its own, Claude won't hold one style across ten designs, so the article describes a Build to Launch skill that takes an article plus a brand profile (fonts, colors, styles) and builds the kit on brand, handing back editable Canva files and PNGs without touching the Canva UI. It runs two ways: inside the Build to Launch MCP for premium members, or downloaded and dropped into Claude, ChatGPT, or any agent that takes a skill. The workflow is set the brand once and let it hold: the first run captures colors as hex, a header and body font, and an optional logo and footer, then every run after reuses that profile. You can steer mid-run (swap a background for the hero image under a gradient) and request one piece at a time (a checklist graphic, a comparison table, a quote card).

A practical core of the guide is that the Canva MCP exposes close to forty tools but, on a free plan, only five matter: `import-design-from-url` (the workhorse, turns a public HTML page into an editable Canva design, no AI credit), `export-design` (renders to PNG, JPG, or PDF, one call per carousel page, works on free even when the editor's download button doesn't), the edit cycle (`start-editing-transaction`, `perform-editing-operations`, `commit`) for swapping text, recoloring, and repositioning, `copy-design` to clone and reskin, and `upload-asset-from-url` to push in a logo or photo as a fill.

The closing section maps where the free plan stops so the walls are clear before you hit them: Canva's built-in AI generation caps at ten uses (this workflow avoids it entirely), resizing a finished design is Pro (generate at the target size from the start), transparent PNG export is Pro (the one wall that's hard to dodge if you need cutouts), and the native Brand Kit is locked, which is why the skill keeps the brand profile in a markdown file instead.

## Key Sections

- What the Canva MCP Gives You (connector basics, two-step free setup)
- Creating Infographics, Carousels, and Charts From One Article (every format, multi-slide carousels, custom backgrounds)
- The Skill That Makes the Canva MCP Effortless (on-brand repeatability)
- Run It, Step by Step (Build to Launch MCP path and the download path)
- Make It Yours (set the brand once, keep evolving it)
- Forty Tools, Five That Matter on Free
- Where the Free Plan Stops (the Pro walls and workarounds)
