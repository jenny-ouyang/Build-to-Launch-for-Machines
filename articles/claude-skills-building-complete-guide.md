# How to Build a Claude Skill That Works

**URL:** https://buildtolaunch.substack.com/p/claude-skills-building-complete-guide
**Track:** AI Builders Playbook
**Published:** 2026-05-21

## Summary

Most Claude skills don't fail because the author stopped paying attention. They fail because of where the rules live. Claude reads the instructions at the top of a skill first, before it knows the task, then starts executing. By the fourth step the early rules have faded from focus even though they're still in the file. Piling more rules at the top just adds more to forget. The skills that hold up aren't the ones maintained most carefully, they're the ones built with the right structure from the start. This guide walks the full build sequence, refined on one real skill across 14 evals.

A skill is three parts, and each part fails in its own way: a short metadata block, the instruction body, and optional supporting files. The description is the only thing Claude reads to decide whether the skill runs at all, so it has to name the moment it should fire as a condition and front-load that trigger. Get this one field wrong and the skill never wakes up. Before writing the body, pick the right type. Two axes (who drives the skill and whether the work is sequential or dynamic) produce four types: checklist, diagnostic, automation, and guiding/mentor. Build the wrong type and you rewrite the body, because a checklist skill can't evaluate its own output and a guiding skill built as a checklist stops at the exact moment it should route.

The body does three jobs: dispatch to the right path, sequence the steps on that path, and embed each constraint at the point it has to fire. The core move is to put each rule where it fires rather than at the top, dispatch before running, and give every step four parts. References are the supporting files pulled only when a step calls for them; a good reference architecture loads only what the current task needs and makes each loaded file something Claude can actually parse. One trap covered in depth: even a loaded rule can still get ignored, and the fix is structural, not more emphasis.

Testing a skill means writing evals: structured test runs that define what good output looks like, run the skill, and return a graded pass or fail with a reason. The guidance is specific. Grade the whole deliverable rather than a slice, don't let the skill grade its own homework, and prefer fewer assertions that discriminate over more that overlap. Fix the skill before re-grading. Maintenance is about catching three kinds of decay, each with its own fix: structural debt inside one file (consolidation pass), sprawl across too many files (consolidate by domain), and version drift after a model update (re-run the evals). Skills don't decay on their own, but skip the upkeep and they degrade with no obvious cause.

## Key Sections

- How Claude Skills Work
- How to Write a Claude Skill Description That Triggers
- How to Pick the Right Claude Skill Type (four types across two axes)
- How to Build a Claude Skill Body That Executes
- How to Structure Claude Skill References
- How to Test a Claude Skill (evals)
- How to Maintain a Claude Skill After It Ships
- Next Steps
