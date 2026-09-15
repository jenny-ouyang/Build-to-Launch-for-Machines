# How to Build a Claude Code Routine That Repeats Your Work
**URL:** https://buildtolaunch.substack.com/p/claude-code-routines-beginner-guide
**Track:** AI Agent Systems
**Published:** 2026-09-15

## Summary

The article opens with a challenge: prove an AI automation works in the shortest possible time, and it uses that challenge to argue against building a long, invisible procedure and hoping the schedule carries it. Jenny's alternative is a five-part map she applies to any recurring job: Input (what the job starts with), Connections (the access it needs), Instructions (the steps and edge cases), Output (what the finished work produces), and Controls (schedule, approval points, receipts, limits, recovery). Before any of that gets scheduled, the map is made physical as a folder — `Claude Automation/` with `SOURCES.md` for approved inputs, `AUTOMATION.md` for the procedure, and `output/`, `feedback/`, and `receipts/` subfolders — so that when something goes wrong later, there is always a specific, inspectable place to look rather than a vague instruction to "automate my research."

The live build proceeds in a deliberately narrow sequence. It starts with a scheduled task that does nothing but say "Good morning," used purely to prove that the task exists, the working folder is correct, Run Now works, and completed runs show up in history — before any real work is at stake. Only after that baseline holds does the session swap in the actual job: retrieving recent public AI articles from Anthropic and OpenAI, saving the raw rows to a CSV, analyzing them, and writing a "Public Signal Brief" alongside a separate receipt file. That first real run happens under direct supervision, with Jenny reviewing the retrieved records, proposed judgments, filenames, and paths before anything gets written, so the approved run becomes a concrete example rather than a specification imagined in advance.

Once that example is approved, the article's central move is capturing it in writing rather than trusting it to memory. Claude records the reviewed sources in `SOURCES.md` and the full working procedure in `AUTOMATION.md`, and the scheduled task itself is then edited down to a small launcher: open `AUTOMATION.md` at the start of each run, follow it exactly, and stop if the file is missing rather than guessing. This split matters because it keeps "when and where" (owned by the schedule) separate from "what" (owned by the file) — so future changes to sources or rules happen in one visible place instead of risking drift between a scheduling interface and a remembered conversation.

The proof step is where the piece earns its practical weight: every run is checked against three separate records — the useful output, a receipt naming the run ID and file paths, and the routine's run history — because a chat claiming a task ran is not the same as evidence that it did. During the live session this distinction mattered directly: one run completed cleanly and produced a second matched output-and-receipt pair, while a later run stopped mid-way when the account ran out of usage credits, and only the history view made the difference between the two outcomes visible. An optional seventh step describes personalizing the routine by swapping in exactly one new source while holding the topic, rules, and output format fixed, so that any change in results can be traced to the one variable that moved, with a fresh run ID protecting the earlier evidence from being overwritten.

The article closes by widening the lens past this one example. Responding to a participant's question about how long the whole system took to build, Jenny's answer is that the first bounded job is often doable in under an hour — the harder discipline is stopping to write down what worked instead of moving on once it runs once. It offers a list of other jobs the same five-part map could cover without needing a connector yet — sorting screenshots, triaging a Downloads folder, indexing new PDFs, flagging recordings for review, building a weekly digest, or surfacing duplicate files before deletion — plus a pointer to a 100-job "Automation Opportunity Atlas" for readers choosing their own first target. This piece is framed as the first of a five-part series that will go on to add connectors, version control, remote execution, and a feedback loop to the same routine, with today's installment deliberately confined to proving the smallest local version before any of that access is introduced.

## Key Sections
- What Makes a Claude Automation Repeatable?
- Build a Working Baseline You Can Inspect
- Keep the Routine Easy to Review and Update
- How to Build the Claude Code Routine in 7 Steps
- Can Non-Engineers Build Claude Automations This Way?
- What Else Can You Automate With the Five-Part Map?
- Start Here: Choose One Job Claude Can Repeat
- Session Timeline
