---
name: analyse-content
description: Analyses one or more pieces of existing content, videos, images, PDFs, links, markdown, or any accessible format, identifying their direction, goal, purpose, and observable success signals, then recommends how the underlying approach could be adapted into the user's own context to produce content for them. Use whenever the user wants to analyse, break down, or learn from existing content (competitor posts, viral examples, articles, videos), asks "what can I learn from this," or wants to understand why something worked before adapting the approach. Supports batches of multiple pieces in one pass. Requires creator-context to be active for persona and profile, so recommendations are grounded in the user's actual context rather than generic advice. Stops at the recommendation, does not draft content automatically, the user decides whether and how to act on it.
---

# Analyse Content

Takes existing content, the user's own past posts, a competitor's work, something that went viral, an article they admired, and breaks down what it's actually doing, then recommends how that underlying approach could translate into the user's own context. This is analysis and recommendation only. It does not draft new content automatically, that's a deliberate boundary, see below.

## Before analyzing

Confirm `creator-context` is active for persona and profile. Recommendations here are only useful if they're grounded in the user's actual field, audience, and goals, without that, this skill can describe what the source content does, but can't meaningfully recommend how to adapt it for someone specific.

## Accepting input

Accept whatever the user provides: an uploaded file (video, image, PDF), a link, pasted markdown or text, or a description alongside an upload. Actually read, view, or fetch the content itself before analyzing, don't work from a title or a user's summary of it alone.

**Batches**: this skill supports multiple pieces in one pass. If the user provides several, analyze each individually first, then look across them for patterns (a shared structural choice, a recurring hook style, a common thread), don't just average them into one vague summary. Present per-piece findings before any cross-piece pattern, so the user can see where a pattern is actually supported by multiple examples versus present in just one.

## Step 1: What is this content actually doing

For each piece, identify:
- **Format and structure**: what kind of piece is this, specifically (a listicle, a personal narrative, a data-driven breakdown, a tutorial, a hot take), not just "a LinkedIn post" or "a video"
- **Direction/goal**: what is this piece trying to accomplish, teach something, provoke a reaction, build authority, sell something, entertain
- **Purpose within its own context**: who is this for, and what problem or interest is it addressing for that audience

State this back before moving further, so a misread gets caught early rather than compounding into the recommendation.

## Step 2: What signals suggest it worked (or didn't)

Look for observable signals within the piece itself and any data the user provides:
- **Structural signals**: a strong hook, a clear payoff, a satisfying structure, a memorable specific detail, these are visible in the content itself regardless of engagement numbers
- **Provided metrics**: if the user shares actual performance data (views, engagement, comments), incorporate it, but don't assume or invent numbers that weren't given
- Be honest about the limits of this analysis: without real analytics, this is an informed read of craft, not a guarantee of what actually drove performance. Say so rather than implying more certainty than is warranted.

## Step 3: Recommend, don't assume the read is correct

Propose specific ways the underlying approach (not the surface content) could translate into the user's own context, given their confirmed persona, niche, and audience. Ground every recommendation in something concrete from the analysis, not a generic "you could do something similar."

If translating the approach requires interpreting *why* something worked, and that interpretation isn't obvious or confirmable from the piece alone, present it as a read to check, not a fact, same principle as the rest of this system: propose, don't assert.

## Presenting output

For each piece: a short summary of what it is, its direction/purpose, and observable signals, followed by the recommendation for how the approach could translate. For batches, close with any genuine cross-piece pattern, clearly labeled as a pattern rather than restated individually.

**Stop here.** Do not proceed to draft content based on the recommendation, even if the next step feels obvious. Ask whether the user wants to act on the recommendation, and if so, whether that means handing off to `social-copywriting`, `content-calendar`, or somewhere else, let them decide the next step rather than assuming the analysis was actually a request to write something.
