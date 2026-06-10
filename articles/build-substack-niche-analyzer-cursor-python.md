# Build a Substack Niche Analyzer With Python and Cursor: The App That Started as My Own Research Tool

**URL:** https://buildtolaunch.substack.com/p/build-substack-niche-analyzer-cursor-python
**Track:** Products Built and Shipped
**Published:** 2025-02-24

## Summary

This is the full build log for a Substack niche analyzer — a tool that takes a keyword, shows subscriber distribution across newsletters in that niche, and surfaces the top performers. It began as Jenny's own research tool and grew into a shippable app. The stack is Python and Next.js, built with Cursor against real Substack API endpoints, and the story includes the deployment bug that broke everything before a database-first approach fixed it.

The build is structured as six steps. It starts by defining what the tool needs to do, then finding the Substack API endpoints that supply the data — the unglamorous discovery work that determines whether the whole thing is possible. From there it covers choosing the stack and a decision that shapes the rest of the app: storing the data locally instead of querying Substack live, so the dashboard stays fast and doesn't hammer the API on every request.

With data in place, the article builds the dashboard that turns raw newsletter numbers into something readable — subscriber distribution and top performers by niche. Then it hits the wall most builds hit at the end: the Vercel deployment failure. The piece walks the debugging of that failure and why the database-first design is what ultimately made deployment work.

It closes with a "what I'd build differently" reflection. The recurring lesson is that the hard parts of a data app aren't the visible features — they're finding the right endpoints and deciding how data is stored, and getting those two right is what separated a working tool from a broken deploy.

## Key Sections

- What you need
- Step 1: Define What the Tool Needs to Do
- Step 2: Find the Substack API Endpoints
- Step 3: Choose the Stack
- Step 4: Store the Data Locally — Don't Query Live
- Step 5: Build the Dashboard
- Step 6: Debug the Vercel Deployment Failure
- What I'd Build Differently Today
