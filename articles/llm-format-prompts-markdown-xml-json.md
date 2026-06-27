# LLMs Don't Read, They Parse: How to Format So AI Actually Uses Your Words

**URL:** https://buildtolaunch.substack.com/p/llm-format-prompts-markdown-xml-json
**Track:** AI Builders Playbook
**Published:** 2026-06-26

## Summary

The core argument is that a language model does not read a prompt or document top to bottom the way a person does. It tokenizes the text and leans on structural cues, headings, blank lines, bullets, to find where one piece of information ends and the next begins. A 2025 study (SepLLM, arXiv 2412.12094) found that separator and punctuation tokens pull a disproportionate share of the model's attention, more than the meaningful words between them. A boundary is a handhold the attention actually grabs, which is why a rule buried in the middle of a long file gets skipped even when the wording is clear. The same words written as a wall of text and as labeled sections carry different amounts of signal.

The guide turns that mechanism into five formatting moves. Separate the kinds of information (instructions, context, examples) into distinct blocks rather than fusing them into one paragraph. Draw the boundary with the lightest tool that works, Markdown headings first (OpenAI's GPT-4.1 guidance), then XML tags when the blocks get long or need harder walls (Anthropic recommends this so Claude can parse each block unambiguously). Put the most important instruction where attention concentrates, at the edges, especially the top. And say what to do rather than what to avoid: a 2026 study (arXiv 2601.08070) found "don't do X" instructions failed more under pressure, because naming the forbidden thing pulls attention toward it.

On format choice, the article frames four options by job. Markdown and XML are for talking to a model; JSON and YAML are for handing it structured data. There are no magic tags, the point is consistent, findable boundaries, not the syntax.

The final section points the same principle outward to AI citation. When someone asks ChatGPT or Perplexity a question, the model quotes pages it can parse cleanly and lift in pieces, the same physics as a prompt. Semantic HTML with real headings, lists, and tables (plus structured data underneath) is the boundary system a crawler reads, and citation research correlates tables with being pulled more often. The closing instruction is concrete: open your CLAUDE.md and move your single most important rule to the top, where position, a clean boundary, and a do-this phrasing all combine.

## Key Sections

- Why does it matter if AI can read your writing? (AI as your tool, and AI as your distribution)
- How does AI read your text? (parsing by boundaries; the SepLLM attention finding)
- How do you write so AI follows it? (the five formatting moves)
- What formats do LLMs like to read: Markdown, XML, JSON, or YAML?
- How do you get cited by AI? (semantic HTML, tables, citation patterns)
- What's next for you (move your top rule to the top; do-this over don't-do-X)
