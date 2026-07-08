# Obsidian + Claude Code: How to Build a Second Brain that Remembers, Connects, and Runs Itself

**URL:** https://buildtolaunch.substack.com/p/claude-code-obsidian-second-brain
**Track:** Hands-on AI Technology
**Published:** 2026-07-01

## Summary

Most AI memory is linear. ChatGPT, Claude, and agent frameworks all remember, but they remember as a running log: each new thing pushes the old ones down and eventually out. That log can't answer the question that matters most for real work — pull up one topic across your whole history, showing what you thought, what you researched, what others said, how it evolved, and where every file lives. This article walks through building a second brain that can answer it: a folder of Markdown notes in Obsidian, wired to Claude Code, that Claude can read, write back to, navigate, and keep in sync.

The case for pairing Obsidian with AI rests on four properties. Claude can read the vault directly because it is plain Markdown on disk. The vault keeps getting fed as you work, so it grows instead of resetting. Claude writes back into it — creating notes, linking them, building dashboards — so the system compounds. And Claude can navigate a large vault without drowning, using structure and search rather than loading everything at once. Together these turn a static note pile into a queryable, self-maintaining knowledge base. The article shows what that looks like in practice: pulling one topic from everywhere, turning a cluster of notes into a dashboard or a map, and letting the graph connect itself.

Setup is four steps: install Obsidian, turn on the command line (Claude Code), install the Obsidian skills so Claude knows how to operate the vault, then run it once to see it work end to end. From there the article covers the recurring vault jobs you hand to Claude — connecting loose notes into the graph, turning a cluster into a saved view, and making Claude check the vault automatically via a prompt hook that fires on every message and nudges Claude to search your notes first when a question sounds like it's about your own history.

The back half is about durability. To survive hundreds of notes, the vault needs a few fixed places and a consistent note shape (frontmatter plus predictable sections like Decisions, Open tasks, and Links), so both you and Claude always know where things go. Keeping the vault auto-updating is illustrated with a daily news-scout example that writes fresh notes into the system on a schedule. The payoff is a flywheel: the more the vault is fed, linked, and pruned weekly, the more useful Claude's answers across it become — a second brain that remembers, connects itself, and increasingly runs on its own.

## Key Sections

- What Makes Obsidian So Good?
- Why Do Obsidian and AI Work Together? (Claude reads it, the vault keeps getting fed, Claude writes back, Claude navigates without drowning)
- What Does a Connected Obsidian + Claude Second Brain Look Like? (pull one topic from everywhere, cluster to dashboard, let the graph connect itself, cluster to map)
- How Do You Connect Obsidian and Claude? (install Obsidian, turn on the command line, install the Obsidian skills, see it work once)
- How Do You Get Claude to Do the Vault Work for You? (connect loose notes, cluster to view, auto-check the vault via a prompt hook)
- How Do You Structure a Vault That Survives Hundreds of Notes? (a few fixed places, one shape per note)
- How Do You Keep an Auto-Updating Vault in Sync? (the daily news scout example)
- Why It Becomes a Flywheel — and pruning it weekly
