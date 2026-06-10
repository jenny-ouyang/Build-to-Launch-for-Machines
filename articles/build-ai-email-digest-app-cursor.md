# How I Built an AI Email Digest App with Cursor

**URL:** https://buildtolaunch.substack.com/p/build-ai-email-digest-app-cursor
**Track:** Products Built and Shipped
**Published:** 2025-03-07

## Summary

This is the full build log of an AI email digest app made in Cursor in a single afternoon — the project that turns an overflowing newsletter inbox into a scored, ranked reading list. It starts from the problem most people recognize: a Gmail tab with more unread newsletters than anyone will read. The app connects to Gmail, extracts the article links, summarizes them, and scores each by quality so the reader sees what's worth their time first.

Before any code, the article shows the spec prompt — the up-front definition of what the app does, its constraints, and its output format. That spec-first habit is the backbone of the build, and the piece reproduces it so a reader can adapt the same prompt rather than starting from a blank page. It also covers the choice of models and tools that the build rests on.

The walkthrough is a clean six-step sequence: connect the Gmail API, fetch unread newsletter emails, extract the article links, summarize them with the Claude API, score and rank the results, and output the finished digest. Each step is a discrete piece a reader can follow and reuse, and the structure keeps the project from sprawling into something unfinishable in an afternoon.

The closing sections add the lessons. There's a "what I'd do differently" reflection, practical notes on using Cursor effectively for this kind of project, and directions for going further. The throughline is that a useful personal tool doesn't require a large engineering effort — a tight spec, the right APIs, and a clear six-step build are enough to ship something that earns its keep daily.

## Key Sections

- What We'll Build / Choice of Model and Tools
- Before you touch code: the spec prompt (what it does, constraints, output format)
- Step 1: Gmail API connection
- Step 2: Fetch unread newsletter emails
- Step 3: Extract article links
- Step 4: Summarize with Claude API
- Step 5: Score and rank
- Step 6: Output the digest
- What I'd do differently / Using Cursor effectively / Going further
