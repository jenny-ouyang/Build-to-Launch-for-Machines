# The 4 Best Research MCPs for Claude (and the Job Each One Owns)

**URL:** https://buildtolaunch.substack.com/p/claude-best-research-mcps
**Track:** AI Agent Systems
**Published:** 2026-06-15

## Summary

Most people pick one scraping tool, point it at everything, and then blame the tool when it hits a wall. The real problem is using a single tool for a job a different one owns. This guide names four research MCPs for Claude and assigns each the one job it does best, drawn from testing all four across 15 platforms (Reddit, Amazon, YouTube, Hacker News, Product Hunt, and more) with real runs, real costs, and the free-tier limits that actually hold.

The four jobs are find, match, extract, and read. Tavily is a search API built for LLMs: one call returns ranked, cleaned snippets with URLs, making it the fastest of the four for mapping where a conversation lives. Its limit is verbatim quotes, so it works as a pointer, not a payload. Exa is a neural search engine that ranks by meaning rather than keywords, surfacing the complaint a builder could never have keyworded, with the best signal-to-noise of the four. Its two weak spots are vague fragments and freshness, since it serves a crawl cache rather than a live fetch.

Apify is the only one of the four that walks through a login wall. It is a marketplace of single-site "actors" running in the cloud, and two facts decide whether a run returns data or bills for nothing: the proxy (datacenter actors are cheap and blocked; residential actors cost more and get through) and the handoff (a run returns a datasetId, and you must call get-dataset-items to pull records). It is also the only tool here that genuinely costs money, with empty datacenter runs still billing a start fee. Firecrawl runs a real headless browser to turn an open URL into clean markdown, which is why it nails open pages like Hacker News and Product Hunt and fails by design on every login-walled or engine-blocked platform.

The piece closes with a routing card built on two checks: do you already have the exact open URL (then Firecrawl reads it), and is the source behind a login or heavy JavaScript (then search and Firecrawl both fail and you need Apify). A 15-platform verdict lists what yielded clean data versus the dead ends, so readers avoid wasting a run. Next steps scale by level: beginners install one MCP on its free tier, intermediates chain Tavily into Firecrawl, and advanced users build the routing reflex.

## Key Sections

- Why one tool hits wall after wall (login walls, engine-level blocks, billable zero-row runs, snippets-only)
- Tavily, Exa, Apify, Firecrawl: one for each job (find, match, extract, read)
- Tavily: mapping the territory fast, install command, free tier, where it breaks
- Exa: finding the complaint you can't name by meaning, the freshness trust check
- Apify: cracking locked platforms, proxy and datasetId mechanics, the real-cost asterisk
- Firecrawl: reading any open URL as markdown until the free credits run out
- The Routing Card: pick the right MCP in 30 seconds, plus the 15-platform verdict
- Next steps by level: beginner, intermediate, advanced
