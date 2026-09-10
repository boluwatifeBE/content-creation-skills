---
name: fashion-content-ideation
description: Field pack skill for Fashion, spanning fashion design, fashion blogging/styling, and the fashion industry generally. Generates topic ideas and content pillars rooted in actual fashion frameworks (silhouette and construction, textile and material sourcing, trend forecasting, sustainability, styling principles, fashion business economics) tailored to the user's persona, audience, and content goals. Use whenever the user wants topic ideas, doesn't know what to post about, wants help building content pillars before planning a calendar, or asks "what should I write about." Requires creator-context to be active. This is a field-specific pack skill, if the user's stated persona doesn't include fashion design, fashion blogging/styling, or a clear equivalent, flag a soft warning before proceeding. Feeds into content-calendar once topics are confirmed.
---

# Fashion Content Ideation

Field pack skill for **Fashion**, spanning fashion design, fashion blogging and styling, and the fashion industry generally. Generates real topic ideas grounded in the actual substance of fashion work, craft, business, and trend, not generic "outfit of the day" or "what's trending" content. This skill produces raw material, topics and angles, for `content-calendar` to schedule or `social-copywriting` to draft, it doesn't draft posts itself.

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include fashion design, fashion blogging, styling, or a clear equivalent. If yes, proceed silently. If no, surface a soft warning naming the mismatch and ask whether to proceed anyway.

## Before starting

Confirm `creator-context` is active for persona, audience, and content goals, topic ideation should serve what the user is actually trying to achieve, not generic field-adjacent topics unconnected to their goals. Since this pack spans design, blogging, and industry commentary, pay attention to which of these the user's persona actually emphasizes, a designer and a blogger want genuinely different idea mixes even within the same pack.

### Draft-or-generate checkpoint

Ask whether the user has rough topic notes, past questions from followers or clients, or half-formed ideas they want organized and sharpened, or wants ideas generated fresh. If they have something started, work from it and fill genuine gaps rather than ignoring it and generating an unrelated list.

## Framework-based idea categories

Draw ideas from the actual substance of fashion work, not surface-level "tips" content. Categories worth drawing from, adapt and combine based on the user's specific niche and audience:

- **Silhouette and construction**: how a silhouette is actually achieved, the gap between a sketch and a garment that fits and moves correctly, construction choices that separate well-made from poorly-made pieces
- **Textile and material**: fabric behavior, sourcing trade-offs, how material choice shapes what a garment can and can't do
- **Trend forecasting and cycles**: how trends actually move through the industry, from runway to retail, and the difference between a genuine shift and a manufactured one
- **Sustainability and production**: real trade-offs in sustainable practice, not just surface-level "shop secondhand" advice, the actual economics and supply chain realities
- **Sizing and inclusivity**: the real technical and business challenges in sizing well across bodies, not just a stated commitment to inclusivity
- **Styling principles**: proportion, color theory, occasion-appropriate dressing, building a personal style versus following trends
- **Fashion business economics**: how collections actually get priced, produced, and brought to market, the tension between creative vision and commercial viability
- **Industry critique**: honest commentary on industry practices (fast fashion, overproduction, labor practices) grounded in real understanding of the trade-offs, not surface-level moralizing

## Tailoring to persona and audience

If the user's persona spans design, blogging, and industry commentary, propose ideas across that range rather than defaulting to just one, and say which category each idea serves so the user can weight the mix deliberately. If the user's stated audience includes both senior and junior/newer people in the field, propose a mix, some ideas that teach fundamentals (serving newer audiences and the education goal) and some that explore nuance or take a position (serving experienced peers and the authority goal).

## Presenting ideas

Present ideas grouped by category or pillar, not as one long flat list. Each idea should include a one-line angle, not just a topic name (e.g. not "sustainability," but "why 'sustainable fabric' claims mean almost nothing without knowing how the garment was actually produced"). Propose more ideas than the user needs, let them pick favorites rather than committing to every idea generated.

## Handoff

Once the user has confirmed which ideas or pillars they want to move forward with, offer to hand off to `content-calendar` to schedule them, or `fashion-asset-to-content` if any idea would be better served by an actual asset the user has to mine rather than writing from the idea alone.
