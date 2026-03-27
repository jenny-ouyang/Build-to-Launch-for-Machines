# How to Install OpenClaw and Run Your First Autonomous Agent

**Published:** March 25, 2026  
**URL:** https://buildtolaunch.substack.com/p/openclaw-setup-guide  
**Engagement:** 34 likes, 0 comments, 5 restacks  
**Word count:** 3,924  
**Status:** Paid article

---

*Complete walkthrough for local and cloud installation — plus the cron job that messages you without being asked*

Most OpenClaw setup guides stop when the gateway starts. Getting to an agent that actually does things (runs cron jobs, messages you on Telegram, operates on a schedule) takes four steps most tutorials skip entirely.

This covers all of them: local and Oracle ARM install side by side, identity files that constrain the agent safely, Telegram including the pairing step the wizard doesn't mention, and your first cron job firing without you asking.

## What "done" actually looks like

Most OpenClaw tutorials declare success the moment the gateway starts. That's step one. There are three more.

The complete loop has four stages:

> Your machine → OpenClaw gateway → Telegram → you

Done means all four are working:

1. **Gateway running** — installed, starts cleanly, `openclaw gateway status` shows `runtime: running` and `RPC probe: ok`
2. **Identity configured** — SOUL.md, AGENTS.md, and USER.md are filled in with real constraints, not default placeholders
3. **Telegram connected** — you can message the bot and get a response; the bot can message *you* first
4. **Cron job firing** — the agent sends you something without you asking

Stage 4 is the whole point. Everything before it is setup. A gateway that starts but has no identity, no Telegram, and no scheduled work is an expensive chatbot.

## The installation paths

Pick your path. Which install method fits your situation, without the sales pitch:

- **Local (Mac/Linux):** ~20 min setup, not always-on, good for testing
- **Oracle ARM free tier:** ~45 min setup, always-on, best free production option
- **Generic VPS (Hetzner/Vultr/Linode):** $4-6/mo, always-on, same steps as Oracle
- **Railway:** ~$5/mo, always-on (may scale to zero on some plans)
- **Fly.io:** $10-15/mo, always-on, one-command deploy
- **Render:** ~$7/mo, always-on on paid plan, free tier spins down
- **DigitalOcean:** UI currently broken, skip for now

**Just want to try it?** Local. You'll have it running in 20 minutes with zero infrastructure decisions.

**Free and permanent?** Oracle ARM — if you can get one. The always-free tier gives you 4 OCPU and 24GB RAM, but ARM capacity is heavily contested. If you land one, it runs 24/7 without a bill.

**Willing to pay?** Railway or Fly.io for the shortest path. Render works well on a paid plan.

## What most tutorials skip

Five production gaps worth knowing that most tutorials skip entirely:

1. **SOUL.md without hard constraints is incomplete.** The docs show you how to define a personality. They don't tell you what happens at 3am when a cron job hits an ambiguous situation with no explicit rules. A SOUL.md without a hard constraints section is incomplete.

2. **The Telegram pairing step isn't in the wizard.** The first time you message your bot after setup, you won't get a response. You'll see a pairing code. Most people assume the bot is broken and restart everything. The fix: run one command.

3. **Asking the agent to "work on this" and closing the chat doesn't work.** Sessions are stateful only while open. Background tasks need cron jobs with an isolated session target.

4. **For cron jobs: use the UUID, not the job name.** `openclaw cron run "substack-notes-review"` won't work. The UUID is what the scheduler uses internally.

5. **Scoped credentials before you give it database access.** Create a read-only or scoped credential specifically for the agent before connecting to real systems.

---

## Next steps

- Get it running locally (20 minutes)
- Give your agent an identity (SOUL.md, AGENTS.md, USER.md)
- Connect Telegram
- Create your first cron job

Templates and step-by-step setup available in the paid section of this article at Build to Launch.

---

*See the full guide at: https://buildtolaunch.substack.com/p/openclaw-setup-guide*
