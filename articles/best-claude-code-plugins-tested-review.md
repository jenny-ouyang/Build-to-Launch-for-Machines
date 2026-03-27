# Stop Installing Every Claude Code Plugin — Here's How to Tell What's Actually Worth It

**URL:** https://buildtolaunch.substack.com/p/best-claude-code-plugins-tested-review  
**Published:** March 23, 2026 | **Track:** AI Builders Playbook  
**Word count:** 4,976 | **Engagement:** 31 likes

---

## Summary

When Claude Code's plugin marketplace expanded to 101 official plugins, most builders either ignored it or installed everything and wondered why their sessions felt slow. This article fixes that by testing 11 plugins on real work — Jenny's actual writing system, real positioning questions, and a live feature build — rather than demos.

The core finding is that "working" means different things for different plugin types. Content plugins tested on an actual writing system. Business plugins tested on real positioning questions. Coding plugins tested on a real feature build. Each produced different value in different session types — which is why the article's main output is a judgment scorecard rather than a static ranked list.

Results: 4 plugins worth keeping always (they add value regardless of session context), 5 worth enabling situationally (they slow things down when the context doesn't match), and 2 that weren't worth the friction in any tested scenario. Marketplace files for some plugins were broken on first install — the article documents what broke and how to fix it.

The article begins by clarifying what Claude Code plugins actually are, since most builders conflate skills, hooks, MCP servers, and marketplace entries into a single fuzzy category. These are distinct layers with different scopes, update cycles, and trust implications. Understanding the architecture is what makes the scorecard useful — without it, you're just copying someone else's list.

The judgment framework (scorecard) asks: Does this plugin change what Claude Code can do, or just how it presents output? Does it work in the session types you actually run? Does the added capability justify the context overhead? These three questions cut through most plugin noise.

---

## Key Sections

1. **What Claude Code plugins actually are** — Skills vs hooks vs MCP servers vs marketplace entries. Different layers, different trust scopes, different performance implications.
2. **The 11 plugins tested** — Which categories were covered: content, business/positioning, coding, and utility.
3. **What changed (and what broke)** — Specific behaviors observed when running plugins on real work. Marketplace file breakage documented with fixes.
4. **The results: 4 / 5 / 2 breakdown** — Always-on plugins, situational plugins, skip-list plugins.
5. **The judgment scorecard** — Three-question framework for evaluating any plugin before installing.

---

## Key Frameworks

- **Plugin type hierarchy:** Skills (structured instructions) → Hooks (lifecycle triggers) → MCP servers (external tool connections) → Marketplace entries (packaged combinations)
- **Three-question scorecard:**
  1. Does this change what Claude Code *can* do, or just *how* it presents output?
  2. Does it work in the session types you actually run?
  3. Does the capability justify the context overhead?
- **Session-type matching:** The plugin that helps a content session hurts a coding session. Always evaluate against your dominant session type first.
- **Result tiers:** Always-on (4) → Situational (5) → Skip (2)
