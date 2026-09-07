---
name: trend-to-content
description: Takes a current trend, news item, or conversation happening in the user's field, or finds one via search if the user doesn't have a specific one in mind, and proposes a content angle tied to the user's specific expertise. Use whenever the user asks "what's trending in my field," "is there anything I should comment on right now," wants a timely or newsjacking angle, or mentions a specific current event/trend and asks how to post about it. Requires creator-context to be active for persona and niche, so the angle is grounded in genuine expertise rather than a generic take. Distinct from analyse-content (which examines one existing piece of content) since this skill is about timing and current relevance, not adapting a specific source.
---

# Trend to Content

Connects something happening right now, a trend, a piece of news, an active conversation, to the user's actual expertise, and proposes an angle worth posting about while it's still timely. Unlike `analyse-content`, there's no single source piece to break down here, the input is "what's happening," not "here's a thing, learn from it."

## Before starting

Confirm `creator-context` is active for persona, niche, and confirmed expertise. This skill only proposes angles the user is genuinely positioned to speak on, if the persona doesn't establish real standing in the relevant area, say so rather than proposing a take that would read as reaching.

## Getting the trend

Ask the user if they already have a specific trend, story, or conversation in mind, or want this skill to find one.

- **If they have one**: confirm you understand what it is and, if it's something you can verify or add context to, use search to check current details before proposing an angle, since posting about a trend with outdated or wrong specifics undermines the whole point of being timely.
- **If they want one found**: search for what's currently active or being discussed in the user's specific field or niche, not a generic "trending topics" search. Bring back a small number of real candidates (not just one), each genuinely relevant to their stated expertise, and let the user pick rather than assuming which one they'd want to comment on.

## Timeliness and judgment

- **Timing matters**: a trend that's already been thoroughly covered or has cooled off is a weaker opportunity than one still actively developing. Say so if a candidate trend looks past its peak relevance.
- **Stay in the actual lane of expertise**: don't propose an angle on something outside what the user's persona establishes real standing in, even if the trend is popular. A take from someone without genuine relevant expertise reads as opportunistic rather than authoritative, which works against the authority/education goals this system is usually serving.
- **Be careful with sensitive or tragic news**: don't propose treating a tragedy, a crisis, or genuinely sensitive current event as a content opportunity, even if it's technically trending in the user's field. If a trend brushes up against something sensitive, flag that directly and ask whether the user still wants to proceed, rather than defaulting to a take.

## Proposing the angle

For the chosen trend, propose:
- **What's happening**, stated plainly and accurately
- **Why this specific user is positioned to say something about it**, grounded in their actual expertise, not just "this is popular"
- **The angle itself**: what specific point of view or insight they could add that isn't just repeating what everyone else is already saying about it

Present this as a proposal to confirm, not a finished take, per the system-wide propose-don't-assert principle. Ask if the angle feels right, or if the user sees it differently, they may have context or opinions about the trend that should shape the angle more than a generated guess would.

## Handoff

Once an angle is confirmed, stop here and ask whether the user wants to move to `social-copywriting` to draft it, or to `content-calendar` to slot it in for later, don't draft the piece automatically, since timely content often needs the user's own read on urgency (post now vs. schedule) more than most other content in this system.
