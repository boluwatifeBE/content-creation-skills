---
name: fashion-confidential-story
description: Helps turn a real client commission, brand collaboration, or piece of design work into a shareable story by properly anonymizing identifying details, while preserving the actual lesson or insight worth telling. Use whenever the user wants to share something from real client or collaboration work but is concerned about confidentiality, mentions an NDA or embargo, asks "how do I tell this story without naming the client or brand," or is referred here from fashion-case-study-builder or fashion-glossary-explainer when a real example needs anonymizing. Requires creator-context to be active. This is a field-specific pack skill for Fashion, if the user's stated persona doesn't include fashion design, fashion blogging/styling, or a clear equivalent, flag a soft warning before proceeding. Not legal advice, the user is responsible for checking against their own actual confidentiality obligations.
---

# Fashion Confidential Story

Field pack skill for **Fashion**. This exists to solve a real, constant problem in client-facing and collaborative fashion work: some of the most useful stories to tell, a client commission gone sideways, a brand collaboration decision, an unreleased collection detail, are ones the user technically can't tell as-is. This skill helps extract the shareable lesson and rebuild the story around it, without the details that would breach confidentiality.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include fashion design, fashion blogging, styling, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Important limitation, state this upfront

This skill is not legal advice, and it doesn't know the specifics of the user's actual NDA, brand agreement, or embargo terms. It helps apply reasonable, sensible anonymization, but the user is responsible for checking the result against their own actual confidentiality obligations before posting, especially for unreleased collections or pre-show details. Say this plainly before proceeding, don't let the user walk away thinking this skill has verified legal safety.

## Getting the real story

Ask the user to describe what actually happened, the real situation, decision, or disagreement, without worrying yet about what needs to be hidden. Getting the true version first makes it possible to identify what's actually essential to the lesson versus what's just identifying detail that can be changed or removed.

Also ask: do they know of any specific things they're not allowed to share (an explicit NDA clause, an embargo date before a launch or show, a brand's confidentiality policy), or is this a general "better safe than named" situation without a specific known restriction? This shapes how cautious to be.

## Identifying what's actually identifying

Go through the story and flag anything that could reveal who the client or brand is, even indirectly:

- **Client or brand name**, the obvious one
- **Niche or market position**, if narrow enough that naming it narrows down who the client likely is
- **Specific details**: budgets, timelines, unique design elements, anything that could be cross-referenced
- **Unreleased collection or show details before launch**, this carries additional risk beyond ordinary confidentiality, since disclosing pre-show or pre-launch details can breach an embargo with real consequences, treat this category with extra caution
- **Direct quotes attributed to real people**, even without naming them, a distinctive quote can be identifying on its own
- **Dates and locations**, if specific enough to narrow things down

## Anonymizing while preserving the lesson

Offer the user a choice of how much distance they want from the real details:

- **Light anonymization**: generalize the client or brand's identity (a market segment description instead of a name), remove or generalize specific details, keep the rest of the story close to what actually happened
- **Heavy anonymization / composite**: build a more fictionalized version, potentially blending details from more than one real project, so no single real client or collection is reconstructable at all, while the lesson stays intact

Whichever level, the actual insight, what was decided, why, what it reveals about the work, must survive the anonymization. If stripping out details starts to hollow out the lesson itself, say so and ask the user what's actually essential to keep, don't silently produce a vague, watered-down story just to be safe.

## Handoff

Once the story is anonymized to the user's satisfaction, hand off the sanitized version to whichever skill needs it, `fashion-case-study-builder` for a full case study, `fashion-glossary-explainer` for a real example within an explainer, or `social-copywriting` if it's just a standalone story post.

## Presenting the result

Present the anonymized version clearly, and briefly note what was changed or generalized from the real story, so the user can judge for themselves whether it's safe enough to use, rather than just trusting the anonymization pass blindly.
