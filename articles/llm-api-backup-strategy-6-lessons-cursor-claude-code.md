# When Your AI API Goes Down: 6 Backup Lessons From a Real LLM Outage

**URL:** https://buildtolaunch.substack.com/p/llm-api-backup-strategy-6-lessons-cursor-claude-code
**Track:** AI Builders Playbook
**Published:** 2025-01-31

## Summary

This is the full account of a live DeepSeek outage hitting Quick Viral Notes mid-day, with real users in the middle of sessions. The note-generation feature stopped working; the code was fine locally, cURL returned nothing, and DeepSeek's own site was down. What followed was an evening of trying to switch to a backup model under pressure — and discovering how little of a backup plan actually existed. The article turns that night into six specific lessons.

The first lessons are about why swapping a model isn't a drop-in fix. API token limits hit harder than the limits you see in a chat UI. API behavior is not the same as UI behavior, so a model that feels fine in the app can act differently through the API. And models degrade during extended use in the same session, which compounds the problem exactly when you're trying to recover.

The economics are the next wall. Cost per request eliminates most backup options before you even get to test them — GPT-3.5 was reachable as a fallback, but Claude and GPT-4o weren't viable on price for this use case. That constraint is why the outage couldn't simply be patched by pointing at the best available model.

The last two lessons are about users and timing. Users remember your best version, so a forced downgrade reads as a failure even when the app is technically still running. And the decisive one: the backup plan has to be built before the outage, not during it. The piece ends with what Jenny would build differently and the single lesson that stuck — that resilience is a design decision made in advance, not a scramble made live.

## Key Sections

- The app / What this incident involved
- Lesson 1: API token limits hit harder than UI token limits
- Lesson 2: API behavior is not the same as UI behavior
- Lesson 3: Models degrade during extended use in the same session
- Lesson 4: Cost per request eliminates most backup options before you test them
- Lesson 5: Users remember your best version — a downgrade feels like a failure
- Lesson 6: The backup plan has to be built before the outage, not during it
- What I'd Build Differently Today / The One Thing That Stuck
