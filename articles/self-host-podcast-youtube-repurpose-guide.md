# How I Built a Podcast Self-Publishing System in 13 Minutes
**URL:** https://buildtolaunch.substack.com/p/self-host-podcast-youtube-repurpose-guide
**Track:** AI Agent Systems
**Published:** 2026-07-20

## Summary

Jenny wanted more reach for a new YouTube video from her Hermes guide, so she built a system that repurposes each approved video into a podcast and publishes it through an RSS feed she owns. Rather than pay Transistor's Starter plan at $19 a month (or $190 annually), or clutter her newsletter with a duplicate Substack podcast, she had her coding agent build self-hosted infrastructure on Cloudflare. The audio was already cut from the video earlier that day by Claude and Codex. A single prompt handled storage and feed generation for Apple and Spotify. The machine did its part in 13 minutes from building to testing to publishing, and the human work (signups, billing, understanding concepts) took about an hour.

To start you need only four things: one approved audio file (the full path to the MP3), a basic show direction (a working name and one sentence about the audience, with the agent proposing description, category, language, and copy), a domain you control connected to Cloudflare, and an email inbox you can open (Spotify sends an 8-digit ownership code to the email inside the RSS feed). You do not need artwork, a transcript, finished R2 setup, or creator accounts before the build begins. The approach is outcome-first: Jenny gave Codex the result she wanted, a few public choices, and the MP3 location, then it inspected the project, found existing conventions, measured the audio, wrote the RSS requirements, built tests, and paused only when a human decision was required.

The article gives the exact master prompt, a single build brief handed to the agent in one message (replace show name, creator, hostname, and MP3 path). It specifies a public feed at podcast.buildtolaunch.ai/feed.xml, media stored in Cloudflare R2, a small Worker that serves RSS and media with correct Content-Type, Content-Length, HEAD support, Accept-Ranges, and byte-range responses, a one-command local publisher, and no paid host. That master prompt breaks into seven checkpoints. Step 1: the agent inspects the project and returns a system plan naming one feed, one bucket, one Worker hostname, and one publish command. Step 2: it builds the local publishing system (show and episode metadata, RSS generator, publisher, Worker, tests), using a permanent random GUID that never changes and content-hashed immutable media URLs; Jenny approves the pilot copy as editorial sign-off. Step 3: activate R2 (Cloudflare object storage) through the dashboard, then the agent deploys the Worker and custom domain via Wrangler OAuth, proving feed GET/HEAD at 200 and a Range request answered with 206 and exactly 16 bytes (Apple requires range support for streaming and seeking).

Step 4: approve and publish episode 1 through an atomic publish (media uploads under immutable keys first, then one feed manifest gets promoted), with rollback meaning promoting a previous manifest rather than deleting a GUID. Step 5: submit the feed to Apple Podcasts, where the agent audits the feed but the human signs in to Apple Podcasts Connect, adds a new show via RSS, confirms content rights, and hits Publish. Step 6: claim the show on Spotify for Creators using "Find an existing show" and the 8-digit ownership code, never re-uploading the MP3. Step 7 is the repeatable future-episode loop: the agent packages the next episode, preserves each episode's GUID, runs a dry run, and after Jenny approves publishes once to the self-hosted feed, so Apple and Spotify refresh automatically without revisiting either directory.

The RSS-feed-you-own model is the core idea: Apple and Spotify are distribution directories that poll your feed, while the self-hosted RSS feed is the single source, and YouTube stays the canonical full video. Real costs came in at $0 billable: the Cloudflare dashboard showed 19.51 MB stored, 11 Class A operations, and 1.01k Class B operations, all inside R2's free allowance of 10 GB-month, 1 million Class A, and 10 million Class B operations. Receipts from the build include the live feed, an MP3 of 16,914,600 bytes, 7 passing automated tests, and release ID 20260719T090900848Z-75967dab305e. The full sequence is packaged as the Self-Hosted Podcast Agent Kit for paid members.

## Key Sections
- You only need four things to start
- The exact prompt I gave my agent
- Step 1: Your agent inspects the project and plans the system
- Step 2: Your agent builds the local publishing system
- Step 3: Activate R2, then your agent deploys
- Step 4: Approve and publish episode 1
- Step 5: Submit the feed to Apple Podcasts
- Step 6: Claim the show on Spotify
- Step 7: Every future episode, one loop
- What it costs
- The receipts from my build
- The pack you keep
- Next Steps
