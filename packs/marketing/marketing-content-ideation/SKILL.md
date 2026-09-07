---
name: marketing-content-ideation
description: Field pack skill for Business Marketing, spanning paid advertising, email, SEO, content marketing, and marketing strategy. Generates topic ideas and content pillars rooted in actual marketing frameworks (funnel stages, channel strategy, attribution, positioning vs marketing, retention vs acquisition, growth loops) tailored to the user's persona, audience, and content goals. Use whenever the user wants topic ideas, doesn't know what to post about, wants help building content pillars before planning a calendar, or asks "what should I write about." Requires creator-context to be active. This is a field-specific pack skill, if the user's stated persona doesn't include marketing, growth, or a clear equivalent, flag a soft warning before proceeding. Feeds into content-calendar once topics are confirmed.
---

# Marketing Content Ideation

Field pack skill for **Business Marketing**, spanning paid advertising, email, SEO, content marketing, and marketing strategy generally. Generates real topic ideas grounded in actual marketing frameworks, not generic "5 tips to grow your business" content. This skill produces raw material, topics and angles, for `content-calendar` to schedule or `social-copywriting` to draft, it doesn't draft posts itself.

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include marketing, growth marketing, digital marketing, or a clear equivalent. If yes, proceed silently. If no, surface a soft warning naming the mismatch and ask whether to proceed anyway.

## Before starting

Confirm `creator-context` is active for persona, audience, and content goals, topic ideation should serve what the user is actually trying to achieve, not generic field-adjacent topics unconnected to their goals.

### Draft-or-generate checkpoint

Ask whether the user has rough topic notes, past client questions, or half-formed ideas they want organized and sharpened, or wants ideas generated fresh. If they have something started, work from it and fill genuine gaps rather than ignoring it and generating an unrelated list.

## Framework-based idea categories

Draw ideas from the actual substance of marketing work, not surface-level "tips" content. Categories worth drawing from, adapt and combine based on the user's specific niche, channel focus, and audience:

- **Funnel and journey thinking**: how a prospect actually moves from unaware to customer, where funnels commonly leak, the gap between a tidy funnel diagram and how people actually behave
- **Channel strategy**: trade-offs between paid and organic, when a channel fits a business model and when it doesn't, common channel-fit mistakes
- **Attribution and measurement**: the real difficulty of knowing what's actually driving results, common ways attribution gets oversimplified or misused
- **Positioning vs. marketing**: the difference between what a business is (positioning) and how it's communicated (marketing), and what happens when marketing tries to compensate for weak positioning
- **Acquisition vs. retention**: the trade-offs and blind spots in businesses that over-index on one over the other
- **Copywriting and messaging**: what actually makes marketing copy work beyond formulas, the psychology behind why certain messages land
- **Budget and resource reality**: how marketing decisions get made under real constraints, not the idealized version taught in courses
- **Client and stakeholder realities**: the actual working relationship between marketers and the rest of a business, pushback on strategy, misaligned incentives (kept general, not confidential, see `marketing-confidential-story` if the user wants to share something more specific requiring anonymization)

## Tailoring to persona and audience

If the user's stated audience includes both senior and junior people, propose a mix, some ideas that teach fundamentals (serving juniors and the education goal) and some that explore nuance or take a contrarian position (serving seniors and the authority goal). Say which each proposed idea is more likely to serve, so the user can weight the mix deliberately.

## Presenting ideas

Present ideas grouped by category or pillar, not as one long flat list. Each idea should include a one-line angle, not just a topic name (e.g. not "attribution," but "why most attribution models quietly reward whichever channel happens to be last-touch, not whichever one actually did the work"). Propose more ideas than the user needs, let them pick favorites rather than committing to every idea generated.

## Handoff

Once the user has confirmed which ideas or pillars they want to move forward with, offer to hand off to `content-calendar` to schedule them, or `marketing-asset-to-content` if any idea would be better served by an actual asset the user has to mine rather than writing from the idea alone.
