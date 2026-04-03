# How to Start Vibe Coding: The Roadmap Nobody Gave You

**URL:** https://buildtolaunch.substack.com/p/how-to-start-vibe-coding  
**Published:** April 1, 2026  
**Word count:** ~4,635  
**Engagement:** 72 likes, 8 comments

---

## Summary

Most vibe coding guides tell you which tool to install. This article covers the part nobody explains: what happens before and after the install — and why most beginners quit somewhere between 80% done and shipped. Jenny's roadmap addresses the spec habit, the 80/20 wall, and a 5-project arc built from 8 months of real experience moving from ChatGPT → Cursor → Claude Code.

The article is organized around six areas beginners need before they can build consistently.

---

## The Spec-First Habit

Before opening any AI tool, answer three questions in plain sentences: Who uses this? What's the one thing it needs to do? What does done look like specifically? The spec takes five minutes. Without it, AI fills every gap with its own best guess — which is how you end up with an app that runs but doesn't do the thing you wanted.

For multi-session projects, the spec becomes a `CLAUDE.md` file at the project root. Claude Code reads it automatically at the start of every session, preventing context collapse across long builds.

---

## Which Tool to Start With

Two decisions only. Terminal or no terminal: browser builders (Lovable, Bolt, v0, Replit, Base44) are fast for first projects but hit real ceilings when projects need external data or scheduled logic. Claude Code requires a terminal and costs $20/month via Claude Pro, but it has full file system access — what makes Tier 2 and Tier 3 builds possible.

Between Claude Code and Cursor: Cursor works well with existing dev background; Claude Code is the better entry point for non-technical builders building from scratch.

---

## The First Session

The first 30–60 minutes follow a predictable 7-step loop: spec → open tool → paste spec as first prompt → read the output → test the core action → find the first thing that doesn't work → fix it specifically. The session ends when the core action works, not when everything is perfect.

The loop is the job. Debugging isn't failure — it's how vibe coding actually works. The failure is quitting when the output isn't immediately right.

---

## The 80/20 Wall

Around 80% of every first build, something stops working in a way that isn't obvious to fix. This is the wall. Two moves through it: maximal specificity (describe the exact failure with exact context) or start a new session with a CLAUDE.md file that captures what's working and what's in progress. The wall isn't a sign of incompetence — almost every beginner hits it, almost none know it's coming.

---

## The 5-Project Arc

Each project in the progression teaches what the next one requires:

1. **Single-function tool** — learn the basic loop (prompt → output → test → fix)
2. **Data-connected tool** — learn how to connect external information  
3. **Scheduled job** — learn what running without you looks like
4. **Multi-step workflow** — learn how to chain logic across steps
5. **System that runs itself** — combines all four, persists over time

The goal isn't to ship five projects. It's that by project five, you understand what you're building before you start building it.

---

## The Minimum You Actually Need

Not "no code required" and not "learn to code first." The real minimum: a problem you actually want to solve, the ability to describe what you want in plain sentences, and patience with the debugging loop. Technical background helps with speed; it doesn't determine whether you can finish.

---

## Key Sections

1. Write the Spec First
2. Which Tool to Start With
3. Your First Session: What Actually Happens
4. The Wall (the 80/20 problem)
5. The Project Arc
6. The Minimum You Actually Need
