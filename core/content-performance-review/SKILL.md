---
name: content-performance-review
description: Reviews the user's own past posts, pasted in, uploaded, or described, and identifies patterns in what has and hasn't worked, then recommends adjustments to future content strategy. Use whenever the user wants to review their own posting history, asks "what's working," "why isn't this getting traction," wants a content audit, or wants to understand patterns across several of their own past posts before planning what's next. Requires creator-context to be active for persona, philosophy, and goals, so recommendations serve what the user is actually trying to achieve. Distinct from analyse-content (which examines someone else's content for inspiration) and hashtag-and-keyword (which optimizes a single upcoming piece for discoverability).
---

# Content Performance Review

Looks at the user's own past content, not someone else's, and finds real patterns in what's worked and what hasn't, then recommends specific adjustments. This is a look-backward-to-inform-forward skill, distinct from `analyse-content`, which looks at other people's work for inspiration.

## Before starting

Confirm `creator-context` is active for persona, philosophy, and content goals. What counts as "working" depends entirely on the goals already established, a post with huge reach but no genuine engagement might be a success for a visibility goal and a failure for a community goal. Don't evaluate performance against a generic standard, evaluate it against what the user actually said they're trying to achieve.

## Gathering the material

Get the user's actual past posts, pasted text, an upload, or several pieces described across the conversation. Ask for whatever real performance data they have (views, likes, comments, shares, saves, click-throughs), if they have it. If they don't have real metrics, say so plainly and proceed on structural/craft analysis alone, don't invent plausible-sounding numbers or pretend to have engagement data that wasn't provided.

**Batches**: this skill is built around reviewing several posts at once, that's the whole point, a pattern needs more than one data point. Review each post individually first, noting format, topic, structural choices, and any provided metrics, before looking across them for patterns.

## Finding real patterns, not manufactured ones

A pattern needs to be genuinely supported by multiple pieces, not asserted from one example or forced to fit a tidy narrative. Look for things like:
- **Format/structure correlations**: do certain structures (personal narrative vs. listicle vs. hot take) correlate with stronger provided metrics or stronger craft, if no metrics are available
- **Topic/pillar correlations**: do certain pillars or subjects consistently perform differently than others
- **Hook style correlations**: is there a pattern in which opening lines led to posts that (by whatever measure is available) did better
- **Consistency issues**: is the confirmed house style and voice actually showing up consistently across posts, or has it drifted over time, this connects back to what `voice-qa` checks on a single piece, but here the question is whether drift is happening across a body of work

If the posts don't show a clear pattern, say so, a small sample or genuinely mixed results is a real, honest finding, not a failure of the analysis. Don't force a tidy story onto ambiguous data.

## Recommending forward

Based on genuinely supported patterns, recommend specific adjustments: lean into a format or pillar that's working, reconsider one that isn't, tighten a drift in voice, adjust cadence or platform mix. Ground every recommendation in a specific pattern found in step above, not generic content advice unconnected to the user's actual posting history.

Connect recommendations to what's actually actionable: if the recommendation is about future planning, point to `content-calendar`, if it's about a drift in voice, point to `voice-qa` for a tighter check on the next draft.

## Presenting the review

Structure the output as: what was reviewed (how many posts, what timeframe if known), patterns found (each stated with the evidence behind it), anything genuinely inconclusive, and recommendations. Be direct about both what's working and what isn't, a performance review that only says positive things isn't useful, but delivered constructively, this is feedback in service of the user's own goals, not a harsh critique for its own sake.
