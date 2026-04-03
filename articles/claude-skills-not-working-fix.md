# Stop Adding New Claude Skills — Fix the Broken Ones First

**URL:** https://buildtolaunch.substack.com/p/claude-skills-not-working-fix  
**Published:** April 2, 2026  
**Word count:** ~4,551  
**Engagement:** 26 likes, 12 comments  
**Access:** Paid

---

## Summary

73% of 214 community Claude Code skills scored below 60/100 in a 2026 audit. Most failed silently — no error message, just slightly wrong output. The instinct every time is to add another skill to fix it. This article is about why that makes things worse, and the architecture that prevents skill sprawl from the start.

Jenny's own setup reached 192 files with 59 broken references, 20 skills no agent ever called, 30 duplicate definitions, and a 1,239-line legacy command still running alongside the current system. The article documents the cleanup and the framework that prevents it from happening again.

---

## Skill, Command, or CLAUDE.md: What Goes Where

The decision most people skip. Skills are reusable named instruction sets invoked on demand. Commands are one-shot actions with defined inputs and outputs. CLAUDE.md is the persistent project context that loads automatically. Getting the layer wrong is the root cause of most silent failures: skills that overlap commands, CLAUDE.md entries that duplicate skill definitions, commands written as skills with no trigger pattern.

---

## The Two Rules That Prevent Skill Sprawl

Two conventions that stop silent divergence before it starts. The folder shape rule: each skill lives in its own directory with a single SKILL.md and no sideways references to other skill directories. The scope rule: each skill owns one domain, and the boundary is enforced by the directory structure, not by hoping agents read the right file.

---

## How Skills Break Without Telling You

Five violation types that degrade AI output with no error message: broken file paths (skill references a moved or renamed file), orphaned skills (written but never wired to a trigger), conflicting commands (two definitions of the same operation in different layers), scope overlap (two skills both claiming the same domain), and version drift (CLAUDE.md and a skill carrying contradicting doctrine from different moments in time).

---

## The Audit: 192 Files, Zero Warnings Initially

Real violation counts from Jenny's actual setup: 59 broken references, 20 orphaned skills, 30 duplicate definitions, and one 1,239-line legacy command running in parallel with its replacement. None of these surfaced as errors during normal use. The audit script that found them is included in the article.

---

## The Complementary-vs-Duplicate Test

A 10-word check for any two skills: "Do these skills fail in different scenarios?" If yes, they're complementary. If no, one of them is a duplicate. The mental model prevents the pattern where adding a skill to fix a problem creates a second competing definition of the same behavior.

---

## The .claude Architecture Template + Audit Script

Included at the end of the article: a clean .claude directory structure template and the `claude skills auditor` script that scans for broken references, orphaned files, and duplicate definitions.

---

## Key Sections

1. Skill, Command, or CLAUDE.md: What Goes Where
2. The Two Conventions That Prevent Skill Sprawl
3. How Skills Break Without Telling You
4. My Audit: 192 Files, Zero Warnings (Eventually)
5. The Complementary-vs-Duplicate Mental Model
6. Running the Auditor on Your Setup
