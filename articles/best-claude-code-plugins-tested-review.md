# Stop Installing Every Claude Code Plugin — Here's How to Tell What's Actually Worth It

**Published:** March 23, 2026  
**URL:** https://buildtolaunch.substack.com/p/best-claude-code-plugins-tested-review  
**Engagement:** 31 likes, 0 comments, 3 restacks  
**Word count:** 4,976  
**Status:** Paid article

---

*I tested 11 plugins, fixed broken marketplace files, and built a judgment framework. This is what I'd keep, skip, and watch.*

Claude Code's plugin marketplace launched quietly. Soon it wasn't quiet anymore.

Developers started running skills on every session. Marketers installed business plugins and expected them to know their business. Builders stacked MCP servers and wondered why things felt slow.

## What Claude Code plugins actually are

People use "plugin" to mean several different things inside Claude. They do not behave the same way.

A Claude Code plugin bundles one or more of these:

- **Skills** — triggered with slash commands (`/brand-voice:enforce-voice`). Runs once, does its job, stops. Cost: per use.
- **Hooks** — run automatically in the background. They attach to events and fire every time. Cost: every session they're active.
- **Commands** — the management layer. `/plugin install`, `/plugin disable`. Free. Not the plugin itself.
- **MCP servers** — external connections to databases, APIs, file systems. Cost: per query.

## The test design

I tested 11 plugins on real work: content, business, coding, and life sciences. For each, three questions:

1. Where does it work?
2. Where does it break?
3. Does it earn a place in the stack?

I tested on a real feature build: adding tap-to-build sentence exercises to a kids Chinese learning app.

## Plugins I'd keep

### Brand Voice (Content)
**What it is:** Discovers your brand materials, generates guidelines, enforces your voice.

**Where it works:** Most creators have brand guidelines scattered across Notion, Google Docs, and random files. This plugin finds all of it and makes it usable. On my content-engine directory, it found 15 brand documents and 34 products I'd never reviewed for consistency.

**Verdict:** KEEP. One-time discovery + guidelines generation pays back on every article after.

### Feature-dev (Coding)
**What it is:** 7-phase structured feature development. Explores codebase, asks clarifying questions, proposes architecture before implementing code.

**Where it works:** Prevents Claude from jumping to the obvious architecture and proposing what's obvious instead of what's right. The value is changing the shape of the feature before code starts.

On the sentence-exercise feature, two parallel agents explored the system first. The clarifying question that mattered: "Should tiles show only correct options or include decoys?" That one answer eliminated three database tables, migrations, and unnecessary complexity.

**Verdict:** KEEP. Token cost earns back when it prevents building the wrong system first.

### Marketing (Business)
**What it is:** Six-skill plugin for content marketing: SEO audit, drafting, brand review, competitive research, campaign planning, email sequences.

**Verdict:** KEEP. Enable for content planning sessions. Excellent when combined with Brand Voice.

### Explanatory-output-style (Tutorial writing)
**What it is:** Always-on hook. Modifies every Claude response with progressive disclosure, layered explanations, and teaching scaffolding.

**Where it works:** For tutorial writing and technical explainers, this produces exactly the structure you want.

**Where it breaks:** It's a hook, not a skill. It runs on *every* response, adding token cost to every exchange, whether structure helps or not.

**Verdict:** CONDITIONAL KEEP. Strong for tutorials. Too much for everything else.

## Plugins to skip

### Sales (Business)
**What it is:** Ten-skill plugin for sales workflows.

**Where it breaks:** The overlap with Marketing is real. Both plugins claim similar jobs. I ran both on the same competitive-intelligence question. Marketing produced 3 comparable competitors, positioning gaps, and 10+ content opportunities. Sales produced flashy HTML, wrong data, and wrong tier.

**Verdict:** SKIP for content creators. The overlap is too real.

### Productivity (Task Management)
**What it is:** Task management and daily planning.

**Verdict:** SKIP if you have a working system. Try it if you have nothing.

## The evaluation scorecard

Before installing any plugin:

1. **Workflow fit** — Does this solve a problem I still have?
2. **Activation style** — Always-on hook, triggerable skill, or data tool?
3. **Cost shape** — Taxes every session, or only when invoked?
4. **Output quality** — Better than plain Claude?
5. **Overlap risk** — Does another plugin cover this already?
6. **Trust level** — Official, vetted, or found through a directory?
7. **Failure mode** — If this breaks, what does it cost me?
8. **Domain fit** — For my workflow, or for someone else's?

---

*This is a summary. The full article includes detailed breakdowns of all 11 tested plugins, architecture analysis, and the complete decision framework.*

Read the full version at: https://buildtolaunch.substack.com/p/best-claude-code-plugins-tested-review
