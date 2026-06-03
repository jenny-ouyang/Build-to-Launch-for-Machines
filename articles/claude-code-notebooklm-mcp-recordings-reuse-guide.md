# How to Query Any Recording Without Rewatching It (Claude + NotebookLM)

**URL:** https://buildtolaunch.substack.com/p/claude-code-notebooklm-mcp-recordings-reuse-guide
**Track:** Hands-on AI Technology
**Published:** 2026-06-01

## Summary

Most recording libraries are passive archives — courses bought, cohort calls hosted, YouTube channels saved — that never get queried again because the friction of rewatching is too high and AI summaries only describe what's in there without answering specific questions. This guide builds a system that solves the retrieval problem: indexed recordings queryable by specific question, returning cited answers in under 30 seconds.

The pipeline has three parts: NotebookLM indexes uploaded recordings and answers only from what you've uploaded with citations to exact passages; the NotebookLM MCP connects those notebooks to Claude Code so you can query them mid-session without tab switching; and a two-layer prompt structure (content framing + format framing) determines whether you get a cited, actionable answer or another generic summary. The setup takes ten minutes for someone already familiar with MCP configuration.

Four source types are covered with different indexing paths. YouTube videos can be added by pasting the URL directly or via a Claude prompt to the MCP, with optional Perplexity MCP chaining to bulk-add a creator's top videos on a topic. Paid course platforms (Teachable, Hotmart, Circle, Substack Live) use browser DevTools to capture the HLS stream URL, which Claude then passes to ffmpeg with the correct CDN headers to extract audio — a 90-minute lecture becomes a searchable .mp3 in about ten minutes with ten seconds of manual work per video. Meeting recordings from Google Meet or Zoom are even simpler: download the .mp4, ask Claude to extract the audio, upload. The article documents Jenny's use of this workflow on 69 lectures from a $5k writing course and her April cohort call, both now fully queryable.

The query prompt structure has two layers that most users only half-implement. The content frame names your current situation and what you specifically need. The format frame tells the notebook how to deliver the answer — succinct (one sentence), detailed walkthrough, plain explanation, or action list. Without the format frame, you get summaries. With it, you get the one-sentence rule, the exact framework, or the verbatim quote with timestamp. The article also covers repurposing indexed recordings into content: querying your own cohort recordings by article angle to surface participant exchanges and live demo moments, then lifting specific exchanges verbatim rather than paraphrasing — with a worked example showing the query, what came back, and what made it into the published piece.

## Key Sections

- Why recording libraries stay passive (the mixed-knowledge problem and why AI summaries made it worse)
- How the recording-to-knowledge pipeline works (NotebookLM + MCP + prompt structure)
- How to add and organize sources in NotebookLM (notebook structure, naming, what makes a source queryable)
- How to connect NotebookLM to Claude Code (install, authenticate, verify via nlm commands)
- How to index YouTube videos (manual path and MCP path, Perplexity chaining for bulk-adds)
- How to index paid course recordings (DevTools, HLS stream URLs, ffmpeg extraction, hdntl vs hdnts tokens)
- How to index meeting recordings (Google Meet and Zoom paths)
- How to query recordings mid-work (two-layer prompt structure with four format types and worked examples)
- How to repurpose recordings into content (article angle queries, verbatim extraction, copyright boundary)
