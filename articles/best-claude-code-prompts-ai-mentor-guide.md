# How I Hired Hormozi, Welsh, and Koe as AI Mentors in 30 Minutes for Free

**URL:** https://buildtolaunch.substack.com/p/best-claude-code-prompts-ai-mentor-guide
**Track:** AI Builders Playbook
**Published:** 2026-05-18

## Summary

The article starts from a familiar problem: courses bought, barely touched, left to collect dust — not because they were bad, but because applying them required time and sustained attention that never arrived. Going back to read one creator's free newsletter, Jenny realized the frameworks she had paid to access were already public and searchable. The missing piece was not more material but engagement in a loop: a mentor she could actually talk to about her specific situation. The solution is to build AI versions of the mentors you want access to, each specialized where that person is genuinely exceptional.

The method is a 3-prompt, 4-step framework that works on any creator with a content trail. Step one builds the mentor's resume using Creator Scout, which generates a structured brief across 11 layers — identity, offers, content strategy, tech stack, frameworks taught, what to steal, what to avoid, and open questions. That brief feeds everything downstream. Step two gathers the portfolio: the creator's 10 best pieces (20 works, past 50 is noise), prioritizing free material since the most persuasive thinking is the widely distributed stuff. These are imported into NotebookLM as a dedicated notebook per mentor.

A deliberate design choice runs through the workflow: keep Claude and NotebookLM separate. Claude is the reasoning layer; NotebookLM is the mentor's knowledge layer. The mentor's opinions stay isolated and answer only from their source material, not from whatever else you have been asking Claude that week. Step three runs the interview — three sequential queries against the notebook, chained by conversation ID so nothing times out, extracting seven categories: core beliefs, framework mechanics, field crimes, approach and personality, system design, hard nos, and failure patterns, closing with a Quick Reference Card. Step four compresses the raw extraction using one strict rule — every line must change how Claude thinks, decides, or produces, or it gets cut — into a 2,000-to-4,000-token XML profile across nine sections that Claude holds as standing context.

The closing sections cover taking mentors to work (bring them something specific to react to, not "what should I do with my business"), the fact that the framework works for any creator with a content trail (Naval, Sahil Bloom, Steph Smith), and one plot twist: the most important voice in the panel is you. The mentors inform decisions; they do not make them. You are the CEO, they are the advisory board. The skills referenced — Creator Scout, mentor-extractor-raw, mentor-compiler-compress, and the mentor-builder-pipeline that chains extraction and compression in one run — are packaged in the Build to Launch MCP, with prebuilt Hormozi, Welsh, and Koe packs available as a bundle.

## Key Sections

- Why bought courses go untouched, and what a mentor loop actually solves
- The 3-prompt framework: research, interview, synthesis
- Step 1: Build their resume with Creator Scout (11-layer brief)
- Step 2: Gather the portfolio into a NotebookLM knowledge layer
- Why Claude and NotebookLM stay separate (reasoning vs knowledge)
- Step 3: Interview the mentor — 3 passes, 7 extraction categories
- Step 4: Synthesize into a compact working system prompt
- Taking mentors to work: react to something specific
- Works for any creator with a content trail
- One plot twist: you are the CEO, the mentors are the advisory board
