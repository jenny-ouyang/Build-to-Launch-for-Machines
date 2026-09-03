# How I Built a Local Business Finder for Any City and Niche
**URL:** https://buildtolaunch.substack.com/p/built-a-local-business-finder-claude-code-project
**Track:** Products Built and Shipped
**Published:** 2026-08-10

## Summary

Jenny frames the project against the scale of small business in the U.S. — citing an SBA figure of 36.2 million small businesses employing 62.3 million people and producing 43.5% of GDP — and a personal anecdote of a teenage friend charging $500 to build one restaurant's website, to argue that "visible online gap" is a testable, repeatable signal for opportunity rather than a one-off freelance lead. Her own trigger was moving from New England to California and needing a way to find trustworthy local services and community in a new place. She proved the idea manually first: scanning 40 Austin landscapers by hand turned up ten with no real website at all, including one rated 4.9 stars across 19 reviews — proof that strong customer demand and an absent web presence can coexist, and that the gap is something you can verify from public listings rather than guess at.

The system she built to repeat that scan automatically runs on a downloadable starter pack (a board-builder script, sample data, matching prompts, and a sample local website template) connected to Apify's Google-Maps-scraping actor through Claude's Apify MCP connector. The workflow is deliberately gated at every paid step: before running a live search, the agent inspects the actor's current input fields and pricing and shows the exact category, location, result count, and estimated charge for approval — her own 40-business run cost about sixteen cents and completed in under 21 seconds. The raw scan returns seven fields per business (name, listed website, rating, review count, phone, category, and Maps URL), and an empty or Facebook-only website field becomes the first useful signal.

That raw list gets turned into a ranked opportunity board using a fixed point system — the heaviest weight goes to having no website at all, with smaller additions for a Facebook-only presence, a rating under 3.5, a missing review count, and fewer than ten reviews — which she's explicit is a sorting aid, not a verdict on its own. The board's top candidates then go through a website audit stage before anyone treats a listed URL as a real opportunity: the agent checks whether the page actually loads, follows redirects, uses HTTPS, has basic SEO metadata, supports mobile, and offers a visible way to contact, quote, or book, and it's instructed to separate directly observed evidence from interpretation — marking inaccessible checks as blocked rather than assuming the worst, and marking genuinely working sites healthy rather than manufacturing a pitch. In her own audit of five ranked businesses, the results split into a dead domain, a parked placeholder page, an older site with an observable weakness, and one legitimately healthy site that the system correctly told her to leave alone.

Once a single opportunity is chosen, the pipeline builds one private, anonymized landing-page concept from only the facts the scan and audit actually verified — sample business name, sample phone number, an inert contact form, and a visible "private concept preview" label, with no real branding, testimonials, tracking, or payment wiring — so the deliverable can be shown to a prospective client as proof of direction without exposing anyone's real identity or going live prematurely. The article also walks through a set of explicit failure-handling rules: what happens if Apify's output format changes, if a page audit times out (treated as inconclusive, not as evidence of a broken site), if the generated concept accidentally includes an unverified claim (removed automatically), or if a session gets interrupted partway through (the system re-inspects what already exists rather than repeating a paid scan or overwriting a finished artifact).

The article closes by laying out three ways to monetize a single scan — building the actual website for a no-website or dead-site business using a short observational outreach note, setting up an AI phone/booking system as a recurring service for businesses with strong reviews but no way to capture leads, or packaging the ranked research itself and selling it to a freelancer or agency that handles delivery — and then generalizes past those three defaults with a broader "opportunity mapping" step. That step takes the same completed scan, board, and audit and looks for opportunities across seven categories (web services, AI phone/intake systems, research products, recurring monitoring, local events and community connections, personal needs, and ideas tied to the reader's own skills), ranks them by evidence strength, speed to a testable result, repeatability, and realistic value, and only then turns the chosen opportunity into an explicit input-to-outcome workflow before anything gets built, sent, or published.

## Key Sections
- What Local Business Research Revealed About the Opportunities Nearby
- What you need to run the scanner
- Start with the prompt to build the complete scanner
- Step 1: Scan Google Maps for businesses with no website
- Step 2: Score the list so you know who to pitch first
- Step 3: Audit the listed websites for what's actually broken
- Step 4: Build the website with AI in an afternoon
- What to watch out for
- Three ways to get paid from one scan
- Find the opportunities hidden inside your scan
- Run it on your own town
