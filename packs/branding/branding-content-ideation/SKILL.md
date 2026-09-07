---
name: branding-content-ideation
description: Field pack skill for Brand Identity Design and Brand Strategy. Generates topic ideas and content pillars rooted in actual brand strategy and identity frameworks (positioning, brand architecture, competitive analysis, tone of voice, brand equity, naming, rebrand rationale) tailored to the user's persona, audience, and content goals. Use whenever the user wants topic ideas, doesn't know what to post about, wants help building content pillars before planning a calendar, or asks "what should I write about." Requires creator-context to be active. This is a field-specific pack skill, if the user's stated persona doesn't include brand identity design or brand strategy, flag a soft warning before proceeding. Feeds into content-calendar once topics are confirmed.
---

# Branding Content Ideation

Field pack skill for **Brand Identity Design and Brand Strategy**. Generates real topic ideas grounded in the actual frameworks and recurring problems of this field, not generic "post about your work" suggestions. This skill produces raw material, topics and angles, for `content-calendar` to schedule or `social-copywriting` to draft, it doesn't draft posts itself.

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include brand identity design, brand strategy, or a clear equivalent. If yes, proceed silently. If no, surface a soft warning naming the mismatch and ask whether to proceed anyway.

## Before starting

Confirm `creator-context` is active for persona, audience, and content goals, topic ideation should serve what the user is actually trying to achieve (authority, education, leads, and so on), not generic field-adjacent topics unconnected to their goals.

### Draft-or-generate checkpoint

Ask whether the user has rough topic notes, past client questions, or half-formed ideas they want organized and sharpened, or wants ideas generated fresh. If they have something started, work from it and fill genuine gaps rather than ignoring it and generating an unrelated list.

## Framework-based idea categories

Draw ideas from the actual substance of brand identity and brand strategy work, not surface-level "tips" content. Categories worth drawing from, adapt and combine based on the user's specific niche and audience:

- **Positioning and differentiation**: how brands stake out territory, what happens when positioning is vague or copied, real trade-offs in choosing a lane
- **Brand architecture**: how multiple products or sub-brands relate to a parent brand, when to unify vs. separate, naming systems
- **Competitive and market context**: how a brand's choices only make sense relative to what competitors are doing, reading a category rather than a single brand in isolation
- **Tone of voice and verbal identity**: how a brand sounds vs. how it looks, common mismatches between the two
- **Brand equity and consistency**: what's actually being protected when a brand stays consistent, when consistency becomes stagnation instead
- **Naming**: the strategic and legal trade-offs behind naming decisions, why some names age well and others don't
- **Rebrand rationale**: why companies rebrand, what a good rebrand is actually solving for versus a cosmetic refresh
- **Client and process realities**: the actual working relationship between a designer/strategist and a client, decisions that get pushed back on, how disagreements get resolved (kept general, not confidential, see `branding-confidential-story` if the user wants to share something more specific requiring anonymization)
- **Craft and critique**: specific design or strategy decisions worth breaking down, the kind of thing a senior would notice that a junior wouldn't yet

## Tailoring to persona and audience

If the user's stated audience includes both senior and junior people (as it often does in this field), propose a mix, some ideas that teach fundamentals (serving juniors and the education goal) and some that explore nuance or take a position (serving seniors and the authority goal). Say which each proposed idea is more likely to serve, so the user can weight the mix deliberately rather than getting an undifferentiated list.

## Presenting ideas

Present ideas grouped by category or pillar, not as one long flat list, each idea should include a one-line angle, not just a topic name (e.g. not "brand architecture," but "why most brand architecture decisions are really about internal politics, not customer clarity"). Propose more ideas than the user needs, let them pick favorites rather than committing to every idea generated.

## Handoff

Once the user has confirmed which ideas or pillars they want to move forward with, offer to hand off to `content-calendar` to schedule them, or `branding-asset-to-content` if any idea would be better served by an actual asset the user has to mine rather than writing from the idea alone.
