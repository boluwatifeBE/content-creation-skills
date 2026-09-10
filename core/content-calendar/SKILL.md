---
name: content-calendar
description: Plans a content calendar, mapping a core topic per slot and distributing it across multiple active platforms the same day by default (adapted per platform's character limit and tier), rather than one platform per day. Slots can also be marked as carousels, a platform-independent format planned separately from the tier system. Use whenever the user asks to plan, schedule, map out, or organize content, asks for a "content calendar," "posting schedule," "content plan," or wants to see what to post and when across a week, month, or campaign. Requires creator-context to be active first; if it isn't, establish it briefly before planning. Always confirms whether the multi-platform default applies to the whole calendar or whether specific slots are single-platform exceptions. Produces the calendar inline as a table by default, or as a downloadable spreadsheet/document on request or for longer plans.
---

# Content Calendar

Builds a scheduled plan of content across the user's active platforms, working from the persona, house style, philosophy, and profile established in `creator-context`. This skill plans and drafts short pieces (hooks, captions). It does not write full long-form pieces inline, that's `social-copywriting`'s job once a specific calendar entry is ready to be produced in full.

## Before planning

If `creator-context` hasn't been established yet in this conversation, capture the essentials first (format scope, persona, house style, profile) rather than guessing. Don't re-run the full intake if it's already active.

### Draft-or-generate checkpoint (ask before building)

Never assume the user is starting from nothing. Before building the calendar, ask: *"Do you already have some content ideas, topics, or a rough plan you want mapped into a calendar, or should I generate the plan from scratch based on your profile?"*

- If they have something started: work with what they give you. Structure it, fill genuine gaps, and ask before adding topics they didn't mention, don't silently pad their plan with invented pillars.
- If they want it generated from scratch: proceed with the rest of this skill as written below.
- Either way, the calendar is always a draft the user can edit, swap, or redirect, not a final, locked plan.

## Cross-platform distribution model (confirm before building)

The default model in this skill is **one core topic per calendar slot, distributed across multiple platforms on the same day**, not one platform per day. A single day's entry can target X, Instagram, LinkedIn, and any other active platform simultaneously with the same underlying idea, each version adapted to that platform's actual character limit and tier (short-form, platform-native long post, or true long-form article, per `social-copywriting`'s platform table). The only thing that differs across platforms for the same slot is the format and length, not the core message, unless the user wants otherwise.

Before building, confirm this with the user rather than assuming silently: *"By default I'll plan each day's topic to run across all your active platforms at once, adapted per platform. Want that for the whole calendar, or are there specific days or topics that should go to just one platform instead?"*

- If the user wants full multi-platform distribution: every slot targets all active platforms by default.
- If the user wants exceptions: note which slots or topics are single-platform, and treat everything else as multi-platform by default. Always confirm exceptions explicitly rather than guessing which topics "seem like" they should be platform-specific.
- The user can also mix models across a single calendar, some days multi-platform, some single-platform, as long as it's been confirmed rather than assumed.

## Scope confirmation

Confirm scope with the user if not already given:

- **Timeframe**: a week, two weeks, a month, or a specific campaign length
- **Cadence**: how many posts per platform per week (if unknown, default to 3x/week for the primary platform and 1x/week for a long-form platform, and say so)
- **Platforms in scope**: pull from the profile's platform list in `creator-context`. Per the cross-platform distribution model above, most or all active platforms will typically apply to most slots, confirm which platforms are actually in play for this calendar, and which (if any) are exceptions scoped to fewer platforms.
- **Content pillars/themes**: 2 to 4 recurring topics or angles the content should rotate through. If the user hasn't defined these, propose a reasonable set based on their persona and audience, and confirm before building the full calendar.

Don't block on all of this if the user just says "give me a week's calendar," pick sensible defaults, state the assumptions you made in one line, and proceed.

## What each calendar entry contains

For every planned slot, generate:

- **Date** (or day-of-week if no start date given)
- **Format**: whether this slot is a standard post (in whichever tier its target platforms require) or a **carousel**. Carousel is platform-independent, it doesn't consume a platform's character limit since it's posted as images or a PDF, so it can accompany any combination of active platforms rather than being scoped to one tier. Ask the user if a given slot should be a carousel rather than assuming, carousels take more production effort (the user designs the actual slide images) so they're usually planned more deliberately than a quick post.
- **Platforms**: the full list of platforms this slot targets (typically all active platforms, per the distribution model above, unless this slot is a confirmed exception)
- **Pillar/theme** it belongs to
- **Tiers involved**: which format tiers this slot spans, short-form (X, Threads, Story captions), platform-native long post (Instagram/TikTok caption, Facebook, LinkedIn Standard Post), true long-form article (LinkedIn Article, Medium, Substack), based on which platforms are targeted. A single slot commonly spans more than one tier at once, that's expected, not an error.
- **Core idea**: the one underlying topic, angle, or lesson this slot is built around, the thing that stays constant across every platform version
- **Hook line**: the actual punchy opening line, publish-ready, following the house style from `creator-context`. If the house style's formatting model doesn't suit a particular entry, per the per-piece flexibility principle, propose the deviation and why, rather than forcing the default or silently skipping it.
- **Short-form draft**, if any short-form platform is in scope for this slot: a complete, ready-to-post version sized for the tightest applicable limit (e.g. X's 280 characters), which can usually be trimmed further or used as-is for other short-form platforms in the same slot
- **Platform-native long post note**, if any platform in this tier is in scope: flag that a fuller version is needed for this tier and roughly how it should differ from the short-form draft (more room to develop the point, same short-form style), point to `social-copywriting` for the actual full draft rather than writing it out in the calendar
- **Long-form article angle**, if any true long-form platform is in scope: a one to two sentence description of the argument or story, plus a suggested title. Flag it "ready to draft" rather than writing the full body here, point the user to `social-copywriting` when they're ready to produce it in full
- **Visual note**: a short line on what kind of visual would pair with this post (defer to `visual-direction` for a fuller recommendation if that skill is active)

**If this slot is a carousel**: note the working title/hook and a rough slide count instead of a hook/caption/angle, flag it "ready to draft" and point to `social-copywriting` for the full slide-by-slide breakdown with per-slide visual direction, the same way a long-form article angle gets flagged rather than written out in full here.

## Tier interchangeability rule

Platforms sharing the same format tier (short-form, platform-native long post, or true long-form article) are treated as interchangeable within that tier, the same underlying draft can serve any platform in that tier with only minor trimming, unless the user wants platform-specific variants. Across tiers, treat it as the same core idea requiring a genuinely different depth of development, not a resize of the same text, per `social-copywriting`'s tier-specific format specs. Only produce distinct variants for each individual platform if the user explicitly asks for that level of platform-specific nuance.

## Output format

- **Default**: present the calendar inline as a markdown table. Fast to scan, easy to revise conversationally.
- **File output**: produce an actual downloadable file instead of (or in addition to) the inline table when the user asks to save, download, export, or share it, or when the timeframe is long enough (roughly a month or more, or a high posting cadence) that a table in chat would be unwieldy. Default to a spreadsheet for anything the user will likely update or check off over time; use a document only if they specifically want a written/narrative version.
- If unsure which the user wants, default to the inline table and mention a downloadable version is available on request.

## Revising the calendar

Treat the calendar as a living draft. If the user asks to swap a topic, move a date, change a platform, or regenerate one entry, edit just that entry rather than regenerating the whole calendar, unless they ask for a full redo.
