---
name: ux-content-ideation
description: Field pack skill for UX/Product Research and Design, including UX engineering, design-to-code, and AI-assisted design workflows. Generates topic ideas and content pillars rooted in actual UX and research frameworks (usability heuristics, information architecture, research methodology, accessibility, journey mapping, design systems) plus emerging workflow topics like vibe coding and design-to-code, tailored to the user's persona, audience, and content goals. Use whenever the user wants topic ideas, doesn't know what to post about, wants help building content pillars before planning a calendar, or asks "what should I write about." Requires creator-context to be active. This is a field-specific pack skill, if the user's stated persona doesn't include UX, product research, product design, or UX engineering, flag a soft warning before proceeding. Feeds into content-calendar once topics are confirmed.
---

# UX Content Ideation

Field pack skill for **UX/Product Research and Design**. Generates real topic ideas grounded in the actual frameworks and current practice of this field, including its fast-moving edge (AI-assisted workflows, design-to-code), not generic "post about your work" suggestions. This skill produces raw material, topics and angles, for `content-calendar` to schedule or `social-copywriting` to draft, it doesn't draft posts itself.

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include UX, product research, product design, UX engineering, or a clear equivalent. If yes, proceed silently. If no, surface a soft warning naming the mismatch and ask whether to proceed anyway.

## Before starting

Confirm `creator-context` is active for persona, audience, and content goals, topic ideation should serve what the user is actually trying to achieve, not generic field-adjacent topics unconnected to their goals.

### Draft-or-generate checkpoint

Ask whether the user has rough topic notes, past client or stakeholder questions, or half-formed ideas they want organized and sharpened, or wants ideas generated fresh. If they have something started, work from it and fill genuine gaps rather than ignoring it and generating an unrelated list.

## Framework-based idea categories

Draw ideas from the actual substance of UX and product research work, not surface-level "tips" content. Categories worth drawing from, adapt and combine based on the user's specific niche and audience:

- **Usability and interaction design**: heuristics, cognitive load, friction points, the gap between what looks clean and what actually functions well
- **Information architecture**: how structure shapes findability, navigation decisions, card sorting and tree testing, when a taxonomy stops matching how users actually think
- **Research methodology**: quant vs. qual trade-offs, when a method is the wrong tool for the question being asked, common ways research gets misused or oversimplified in practice
- **Accessibility**: real accessibility considerations beyond compliance checklists, what gets missed even by well-intentioned teams
- **Design systems**: consistency vs. flexibility trade-offs, when a design system helps velocity and when it becomes a constraint
- **Journey and persona work**: the gap between a tidy persona document and how real users actually behave, journey maps that look complete but hide the messiest parts of an experience
- **AI-assisted design and vibe coding**: what these tools actually speed up, what they still get wrong, where human judgment remains load-bearing, honest takes on a space with a lot of hype
- **Design-to-code and handoff**: the real friction between design intent and engineering implementation, what a good handoff actually requires beyond a Figma file
- **Client and stakeholder realities**: the actual working relationship between research/design and the rest of an organization, pushback, misaligned incentives, how disagreements get resolved (kept general, not confidential, see `ux-confidential-story` if the user wants to share something more specific requiring anonymization)

## Tailoring to persona and audience

If the user's stated audience includes both senior and junior people, propose a mix, some ideas that teach fundamentals (serving juniors and the education goal) and some that explore nuance, take a position, or challenge conventional practice (serving seniors and the authority goal). Say which each proposed idea is more likely to serve, so the user can weight the mix deliberately.

## Presenting ideas

Present ideas grouped by category or pillar, not as one long flat list. Each idea should include a one-line angle, not just a topic name (e.g. not "accessibility," but "why most accessibility audits check boxes that don't reflect how anyone with a real disability actually uses the product"). Propose more ideas than the user needs, let them pick favorites rather than committing to every idea generated.

## Handoff

Once the user has confirmed which ideas or pillars they want to move forward with, offer to hand off to `content-calendar` to schedule them, or `ux-asset-to-content` if any idea would be better served by an actual asset the user has to mine rather than writing from the idea alone.
