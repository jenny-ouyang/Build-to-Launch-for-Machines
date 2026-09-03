# What Happened When I Let OpenClaw Run My Business for Four Weeks
**URL:** https://buildtolaunch.substack.com/p/openclaw-autonomous-agent-live-demo
**Track:** AI Agent Systems
**Published:** 2026-03-16

## Summary

This article is the write-up of a live office hour where Jenny screen-shared her actual OpenClaw setup — the open-source framework, by then at 273,000 GitHub stars, for running AI agents autonomously — after roughly four weeks of running it in production for her own business. The session's opening hook, and the reason she decided to show the system publicly, was that one of her agents had analyzed two weeks of engagement data across X and Bluesky on its own, updated its own strategy file, and told her to stop posting on X and focus on Bluesky, without being asked. She read it and followed it. That unsolicited strategy pivot is the article's dividing line between a chatbot and an agent: a chatbot responds to what you ask; this system ran on a schedule, evaluated its own results, and rewrote its own instructions.

The piece walks through OpenClaw's core structure — a Persona file defining who the agent is, a Soul file holding its deeper values and decision principles, Skills as markdown files that teach it specific tasks, and a Workspace where it reads and writes its own logs and strategy documents — running on a free-tier Oracle Cloud ARM instance 24/7. It frames most people's AI usage as "Level 1 automation": you re-explain your business, audience, and goals in every fresh chat because the model has no memory between sessions, so you're the one doing all the cognitive labor of holding context. OpenClaw's answer is 18 active cron jobs, each with its own prompt, schedule, and delivery channel, covering social posting three times a day to X and Bluesky, autonomous Bluesky engagement replies, Substack commenting, weekly SEO analysis pulled from Google Search Console, content-pipeline syncing, and monitoring of other autonomous app builds — reached through an MCP bridge plugin since the lightweight Oracle server can't run a browser or heavy tooling locally. She explains why she runs this on Claude's API rather than a subscription plan: per-token billing lets her set an explicit budget per cron job, and subscription rate limits that cut off mid-task (which she watched a fellow builder in the session hit) are untenable for something running unattended around the clock; routine tasks run on Sonnet while strategy-level judgment calls get routed to Opus.

The most detailed case study is the three-phase evolution of her autonomous social agent, nicknamed Clawdia. Phase 1 was pure mechanical distribution — posting article links with no personality. Phase 2 added a human-in-the-loop step where Clawdia drafted replies and queued them in Telegram with approve/skip/edit buttons, waiting for a human decision before anything posted. Phase 3, flipped on only after weeks of refining the persona and rules, gave Clawdia full autonomy to read notifications, judge whether a reply is spam, genuine, sensitive, or a business inquiry, like genuine engagement before replying, ground replies in actual published article content, skip bot accounts entirely, and reflect on her own performance twice a week to update her strategy file. The X-to-Bluesky pivot happened inside that Phase 3 loop: Clawdia noticed Bluesky meaningfully outperforming X, wrote the recommendation into her own STRATEGY.md, and Jenny read it the next morning rather than making the call herself. She's candid that early follower counts (11 to 22 over the tracked window) are noisy and hard to attribute cleanly, but frames the follower number as beside the point — the point is that the agent made the strategic call unprompted.

Two operational threads round out the tour: skills management and memory. Skills — reusable markdown instruction files — live in a GitHub repo rather than scattered locally, which gives her version history and a browsable map of what the agent actually knows, and she flags a real caution about pulling skills from OpenClaw's community marketplace: since they're markdown plus scripts, they should be scanned before use rather than trusted blindly. Memory turned out to be the biggest operational complaint — everything defaults to piled-up markdown files in the workspace, which she describes as "content pollution" once multiple projects are running — and her fix was building a custom Supabase plugin (Postgres under the hood, with semantic vector search) so the agent retrieves relevant context instead of scanning through accumulated files. A closing case study shows a non-technical business partner making live website changes by describing them in plain English inside a shared Telegram group with the agent, which implements the change and deploys it via Vercel autonomously, closing the gap between someone who has an idea and someone who can execute it without either of them touching code.

The article closes with reflections from the two other attendees — a solo vibe coder and an enterprise CIO building agents for hundreds of doctors — both converging on the same point: the underlying data (Search Console numbers, social notifications, article metrics) was never the scarce resource; the new layer is the synthesis and judgment sitting on top of deterministic data, deciding what it means and what to do next. It ends with a concrete starter path for readers: install OpenClaw, stand up one simple cron job, use Telegram as the interface, write a single skill file, and move through Jenny's own Phase 1 → 2 → 3 autonomy ladder rather than attempting full autonomy on day one — plus a list of adjacent builds (a morning briefing agent, competitor monitoring, customer email triage, research synthesis, PR review, and eventually autonomous purchasing) that follow from the same architecture but aren't all running yet.

## Key Sections
- Who was in the room
- The tool: OpenClaw
- Why a cron job beats a chatbot
- What I showed (the full tour)
- Telegram as the front door
- Cron jobs: the real power
- The API cost model
- MCP: connecting to the outside world
- Autonomous social media (the three-phase evolution)
- Weekly SEO analysis, no analyst required
- Skills mapped to GitHub
- Memory management (the biggest complaint)
- Multi-agent collaboration (the James story)
- What I noticed watching them react
- What else you could build with this
- What you can do right now
- Session timeline
