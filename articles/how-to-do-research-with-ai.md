# How to Do Research With AI Effectively: 3 Questions Walked Through Live
**URL:** https://buildtolaunch.substack.com/p/how-to-do-research-with-ai
**Track:** Hands-on AI Technology
**Published:** 2026-04-11

## Summary

This is the recap of the first live session in Jenny's Practical AI Builder cohort, built around a claim that most people are already doing AI research badly: they open a tool, type a vague question, and hope the answer helps, without ever routing the work to the right source or forcing the output into a decidable shape. The article opens by naming three distinct research situations that get treated identically even though they need different handling — learning something from scratch when you don't yet know enough to ask a sharp question, tracking down a specific, current piece of data like a price or a listing, and pressure-testing a thesis you already hold to decide whether it's worth another week of effort. Naming which bucket a question falls into, the article argues, is most of the battle, because a "learning" question that gets treated like a "finding" question (or vice versa) produces generic, unusable output.

On top of those three question types sits a five-stage process that Jenny presents as tool-agnostic: Refine (turn a vague desire into an actual question), Lens (decide whose perspective or vantage point you're borrowing to interpret the answer), Retrieve (route the question to the source that actually holds the relevant data, rather than whatever tool is open), Synthesize (force the raw results into a comparable structure instead of a loose summary), and Decide (end with one concrete next move, not a list of five possibilities). The framework's core discipline is in stages 3 and 4: retrieval only works if you know which tool holds the answer, and synthesis only works if you force the output into something like a table rather than accepting a paragraph of "plausible-sounding" prose.

The session then runs all three question types live, in parallel, using two MCPs connected to Claude: the Perplexity MCP for retrieval against current web data, and a custom Build to Launch MCP that holds pre-built, reusable research skills (named in the article as things like `idea-research` and `data-curator`) so the same multi-phase process doesn't get rebuilt from scratch every time. The "learning" example — "how do I make money with AI?" — got refined into a narrower question about which revenue models top performers in the space actually use, ran through a four-phase Build to Launch MCP workflow (landscape scan, demand signals, top-performer patterns, structured curation), and came back as a comparison table with columns for revenue model, audience size, pricing, and team size; the verdict was that the market is crowded but not closed, and that the people winning build what they teach rather than just talking about ideas. The "finding" example — best deal on a used car — needed no refinement and went straight to Perplexity, returning a decision-ready list of listings and prices rather than a table. The "evaluating" example, a participant's live idea for a deal-tracker app, ran through the same validation workflow on the spot and came back showing the space dominated by an established player; the framing that follows is a useful pattern in itself — a crowded market run by an incumbent isn't necessarily a reason to abandon an idea, it's a reason to reframe it as something that feeds the incumbent's ecosystem instead of competing head-on.

A chunk of the session becomes Q&A, and the article treats those live questions as first-class content rather than an afterthought. On accuracy — one attendee called the process a "black box" that might be cherry-picking data with no way to verify it — Jenny's answer draws a hard line between two layers: the AI overview is directional (it tells you what's worth looking at) and a separately built data-collection pipeline is where the factual claims actually get verified, citing her own Substack Notes MCP as an example where she retrieved raw JSON rather than trusting a model's synthesized summary of the numbers. On storage, the comparison lands on local files and GitHub being best for technical, AI-read-and-write workflows, and Notion being better when structure needs to be accessible to non-technical collaborators across devices. A live Gmail-scanning scheduled task is walked through as a case study in a broader "file pointer" method for automation: writing the full instructions for a recurring task into one authoritative file, then having every session point at that file and execute a named section, which sidesteps the single-folder access limitation of pointing an AI tool at scattered context.

The article closes by turning the whole framework into homework: thirty example questions sorted into the three buckets (learning, finding, evaluating) for readers to swap their own topic into, plus setup instructions for the two MCPs used in the demo. It ends with program logistics — Practical AI Builder is a twelve-month monthly cohort building toward a portfolio of real, shipped outputs — and a note on the accreditation status of a CPD certification track attached to the program, plus a full timestamped session timeline for members with recording access.

## Key Sections
- The 3 Types of Research Questions
- The 5-Stage Research Process
- The Live Demo
- How the MCPs Work
- The Accuracy Question
- Storage: Notion vs. Local Files vs. GitHub
- Gmail Automation: Scanning Newsletters for Ideas
- Scheduled Tasks and the File Pointer Method
- MCP Access and Multiple Emails
- What to Work On This Week
- About This Program
- Session Timeline
