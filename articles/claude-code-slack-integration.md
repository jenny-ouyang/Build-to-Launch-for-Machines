# How I Used Slack as a Two-Way Work Surface for Claude
**URL:** https://buildtolaunch.substack.com/p/claude-code-slack-integration
**Track:** AI Agent Systems
**Published:** 2026-09-02

## Summary

The article opens from a concrete pain point: a daily automated report that triages four Gmail inboxes used to dump everything into one growing Claude conversation, so unrelated jobs — cleaning promotional email, chasing a broken automation, capturing notes for another project — piled up in the same context, and none of it could run while the laptop was closed. Jenny's fix is to route the report through Slack as a two-way surface instead of a one-way notification: she picks one item out of the report, gives it its own Slack thread, and lets Claude work it there, with every question, update, and result returning to that same thread. The core discipline she lands on is "one thread, one unit of work" — if the job or the permission boundary changes, she starts a new thread rather than letting one conversation absorb everything.

She walks through several live examples to show what the setup actually does. Asking Claude to tighten an SEO description on a published article returned a completed, scoped edit in 34 seconds. A request to draft new Substack notes from her existing notes strategy and top-performing data produced 16 drafted notes in about 11.5 minutes — and Claude stopped short of publishing them, explicitly telling her it couldn't push to Substack from that run rather than overreaching. A single vague sentence — floated as an idea about how red-team experiments affect normal users — came back as a developed concept in just over a minute because Claude could pull in existing project context instead of starting cold. On the Gmail side, asked to clean out one inbox, Claude reported that it had found 658 unread Promotions messages dating back to 2014 and stated that number before touching anything, letting her approve or redirect the scope from her phone; a similar cleanup elsewhere stripped an "UNREAD" label from 23 matches in 73 seconds, and another job read one inbox report, logged its action items into her TaskNotes system, and committed the change in about two minutes.

Behind the Slack thread, the actual chain of custody runs through GitHub: a Slack message becomes a GitHub issue or comment, which triggers Claude Code running as a GitHub Action, which posts its answer back into the issue, which a Slack/GitHub subscription relays back into the original thread. Jenny explains why she picked GitHub as the durable workspace rather than keeping everything inside Slack or Claude itself: it preserves full history of what changed and when, one issue gives each job a hard boundary that she can leave and return to without re-explaining anything, and its free tier covers this workflow without adding another subscription. She frames this as a bet that GitHub becomes standard infrastructure for solo operators as more of their work moves to agents.

The setup section walks through connecting the three services in sequence and validating each hop before adding the next: authorizing Slack as a Claude connector from Claude's connectors page; installing the Claude GitHub App via `/install-github-app`, generating a subscription token with `claude setup-token`, and storing it as a repo secret so the Actions workflow authenticates against her Claude subscription rather than a metered API key; and finally installing the GitHub Slack app, linking accounts, and subscribing a channel to both `issues` and `comments` events so replies flow back automatically. She verifies the GitHub-to-Claude half in isolation first with a read-only instruction before ever touching Slack, then proves the full loop with a two-turn test — asking Claude to read a file and report its first heading, then challenging it in a Slack reply to repeat the answer without re-reading the file — which returned in 13 and 21 seconds respectively and confirmed the thread was carrying real conversational state. Gmail access is deliberately added last, after the base loop is already proven, using the same named multi-account connections from her earlier four-inbox setup, with prompts that explicitly restrict each job to read-only retrieval or narrowly scoped writes.

The piece closes with an honest account of the rough edges: the `/github` slash command can't be invoked from inside an existing Slack thread, so new jobs always start from the main channel; a cloud Claude run reads the committed version of a file at HEAD, which once produced a mismatched count against her locally edited working copy; issue threads read only the first 100 comments, so they shouldn't be allowed to calcify into permanent project rooms; and connecting Gmail widens the security surface enough that she calls out revoking the Slack/GitHub app and rotating secrets as the way to shut the loop down cleanly. She ends with a five-step sequence for starting a first bounded job — prove a read-only answer, prove a challenge-and-recheck, add one external tool only once the base loop works, approve one small scoped action, then compare the result against the real system before closing the issue — as the repeatable pattern for everything built on top of this.

## Key Sections
- Turn One Morning Report Into Separate Claude Jobs From Your Phone
- Run Research, Content, and File Changes From One Slack Setup
- What Is Running Behind the Slack Thread?
- Download the Setup Package
- Before You Connect Claude to Slack
- Connect Slack to Claude
- Connect GitHub to Claude
- Connect GitHub to Slack
- The Slack to GitHub to Claude Loop
- Add Gmail Only After It Works
- What Claude in Slack Cannot Do
- Run Your First Bounded Job
