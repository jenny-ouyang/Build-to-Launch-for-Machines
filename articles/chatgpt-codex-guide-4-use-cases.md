# Why I Switched to the New ChatGPT Codex App: 4 Things I Shipped
**URL:** https://buildtolaunch.substack.com/p/chatgpt-codex-guide-4-use-cases
**Track:** AI Builders Playbook
**Published:** 2026-07-22

## Summary

On July 9 OpenAI folded Codex into the new ChatGPT desktop app, so a single download now opens with a top-left picker that switches between ChatGPT (with Chat for conversation and Work for long agentic knowledge jobs) and Codex (the coding agent that reads local files, runs terminal commands, tests code, and hands back accept-or-reject edits). Jenny frames the tools by their roles in her workflow: Claude is the neutral strategist she lived inside all year because its file system let AI read and write real files, while ChatGPT is the creative mentor. Codex adds a strict instruction-following engine bolted onto that creative side, which is what pushed her to stress-test it. She notes the month of rapid shipping behind it (Sites, Import to Codex, Record and Replay, Codex Remote general availability, the July 9 merge with GPT-5.6 and in-app editing, and safer terminal-command handling).

She shipped four real jobs in one week. First, her first long-form YouTube video (14 minutes, published with chapters, captions, and thumbnail) built without ever touching an editor: the app taught her A-roll/B-roll vocabulary, then they built a recording pipeline where Codex watched a drop folder and stitched takes into segments, and it generated thumbnails and images in-app with no extra API cost. It hit real bugs (an invalid video file, nearly treating a half-written file as finished), which she caught only because the app shows every file it touches. Second, she turned that video into a podcast: she handed ChatGPT one approved MP3 and the outcome she wanted, and it researched directory requirements and built the storage, streaming server, RSS feed, episode format, one-command publisher, and tests in a single build, now live on Apple Podcasts and Spotify.

Third, she asked it to visualize her invisible Substack Notes engine. It built three clickable prototypes on real Notes data (a Daily Desk attention queue, a Source Flow provenance board, and a Calendar Studio scheduler), then merged the operating behavior of one with the editorial look of another into a single design and began wiring it to the live engine (27 Notes, 79 sources) behind a read-only path first. Fourth, the quiet money-saver: Codex located an accidentally archived task (correcting itself after checking the wrong one) and pinned it back, turning task history into something the agent operates. She also runs a ChatGPT model as the driver inside her Hermes agent runtime, so background pipeline work bills through her subscription instead of per-call API charges.

A dedicated section covers interface details that made her stay: visible parallel subagents you can open and read, a pixel pet showing live task status, selecting text in a file or highlighting a chat reply to "Add to chat" or leave annotations instead of copy-pasting, and an end-of-task diff view listing every file touched (with lines added and removed) plus which files were only read. She also flags real costs: importing dragged in a pile of unneeded MCP servers (the process pile-up that once overheated her computer, fixed by routing repeated servers through one shared porter), and three long-running high-reasoning tasks burned most of her weekly allowance in a day, so match the model and reasoning level to each job.

Her verdict: the new app is no longer behind Claude Code for her work (it follows tasks, calls tools, runs skills, coordinates agents, holds history, and its visual output is stronger), but she declines to call it a clean scoreboard win without matched side-by-side tasks. Honestly, she did not fully switch. She kept both, because the same skills, MCPs, and scheduled tasks run across Claude and ChatGPT on top of one shared second brain, so you never have to pick the tool when you own the system underneath it. Her recommendation to readers deep in Claude: no pressure to move, but if you want what Codex is good at or your current costs sting, start at twenty dollars a month, audit MCP servers before importing, and size the job to the plan.

## Key Sections
- What the ChatGPT App and Codex Are, and What Just Shipped
- How I Made My First YouTube Video Without Touching an Editor
- Turning That Video Into a Podcast on Apple and Spotify
- 3 Clickable Prototypes for a Workflow I Could Never See
- How Codex Finds Any Task Again and Runs My Pipeline for Free
- The Small Interface Details That Make Codex Nicer to Use
- Should You Move to ChatGPT and Codex Now, or Stay on Claude?
