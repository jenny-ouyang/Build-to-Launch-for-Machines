# Open-Source LLMs in 2026: What's Actually Open, and How to Pick One

**URL:** https://buildtolaunch.substack.com/p/open-source-llms-2026-pricing-hosting
**Track:** Hands-on AI Technology
**Published:** 2026-07-08

## Summary

The popular story is that open-source AI has caught up: DeepSeek, Qwen, and Llama are free, everywhere, and closing the gap on Claude and GPT. That story is true but it hides two things that change what a builder should actually do. First, almost none of these models are open source in the strict sense. Second, the free models are not a gift — they are a competitive weapon aimed at whoever charges for AI, and in 2026 that weapon largely moved to Chinese labs. This guide argues that picking an open model has less to do with the model than with the license it ships under and the host you run it on, and it lays out a field guide that sorts every lab, model, license, host, and metric into one order.

The core confusion is that three different things wear the same word "open." A license, a business strategy, and a hosting bill all call themselves open, and nobody separates them. The article's five-bucket map fixes that: a lab trains a model, the model ships under a license, you run it through one of five hosting lanes, and you judge those lanes on a few numbers (dollars per million tokens, tokens per second, time to first token). Open source, per the Open Source Initiative, requires weights, training-data information, and the code that built the model, under a license permitting any use. Open weight clears a far lower bar — you get the finished weights and a license and little else. Most "open" models, including Llama, are open weight, and the licenses can carry real ceilings (Llama's 700-million-monthly-active-user clause is the example that can quietly bill you).

On who ships open models now and why, the piece explains the strategic logic: giving away a frontier model commoditizes the layer your competitor sells, so open weights function as an attack on closed-model pricing power. That reframes the leaderboard — the reason a Chinese lab tops it is strategy, not coincidence. The guide then gets practical about the two decisions that actually determine cost and risk: how to read a model's license before you ship (what you're allowed to build, where the ceilings sit) and how to pick where the model runs. The same open model can charge four different prices depending on the hosting lane, so it walks through the tradeoffs across serverless-to-self-host options like Groq, Together, and Bedrock, tuned to speed, price, and control.

The closing decision framework helps a builder choose between an open model and Claude or GPT, and lands on a durable point: the model is never the moat. It offers an "open-model decision card" for routing a given job to open versus closed based on volume, license fit, latency, and control, then argues that whatever edge you build has to live in your product, data, and distribution — not in which weights you happened to run. For the target reader, someone already fluent in AI tools but stuck on which "open" model they're actually allowed to build on, the article turns a misleading landscape into a clear, ordered map with a repeatable way to decide.

## Key Sections

- The Open-Source LLM Field Guide: Five Buckets for Every Name (labs, models, licenses, hosting lanes, measuring sticks)
- Open-Source vs Open-Weight: Why Most "Open" LLMs Aren't Actually Open Source
- Who Actually Ships Open Models Now, and Why the Leaderboard Went Chinese
- Why Would Anyone Give Away a Frontier Model? Open Weights Are a Weapon
- How to Read an Open Model's License Before You Ship
- How to Pick Where Your Open Model Runs: Groq, Together, Bedrock
- How to Decide Between an Open Model and Claude or GPT
- The Open-Model Decision Card, and Why Your Moat Is Never the Model
