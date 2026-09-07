---
name: content-calendar
description: Plans a social media content calendar, mapping out hooks, short-form captions, and long-form topics/angles over a given time period, across whichever platforms the user's creator-context profile defines (including custom platforms beyond the built-in defaults). Use whenever the user asks to plan, schedule, map out, or organize content, asks for a "content calendar," "posting schedule," "content plan," or wants to see what to post and when across a week, month, or campaign. Requires creator-context to be active first; if it isn't, establish it briefly before planning. Produces the calendar inline as a table by default, or as a downloadable spreadsheet/document when the user asks to save, download, or export it, or when the plan spans a long enough period that a file is more usable than a chat table.
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

## Scope confirmation

Confirm scope with the user if not already given:

- **Timeframe**: a week, two weeks, a month, or a specific campaign length
- **Cadence**: how many posts per platform per week (if unknown, default to 3x/week for the primary platform and 1x/week for a long-form platform, and say so)
- **Platforms in scope**: pull from the profile's platform list in `creator-context`, including any custom platforms and their stored format classification (short-form or long-form). Let the user override for this specific calendar.
- **Content pillars/themes**: 2 to 4 recurring topics or angles the content should rotate through. If the user hasn't defined these, propose a reasonable set based on their persona and audience, and confirm before building the full calendar.

Don't block on all of this if the user just says "give me a week's calendar," pick sensible defaults, state the assumptions you made in one line, and proceed.

## What each calendar entry contains

For every planned post, generate:

- **Date** (or day-of-week if no start date given)
- **Platform**: pulled from the user's actual platform list, whatever that includes
- **Pillar/theme** it belongs to
- **Format type**: short-form or long-form, based on each platform's stored classification from `creator-context` (built-in platforms have this defined already; custom platforms use whatever classification was captured when they were added)
- **Hook line**: the actual punchy opening line, publish-ready, following the house style from `creator-context`. If the house style's formatting model doesn't suit a particular entry, per the per-piece flexibility principle, propose the deviation and why, rather than forcing the default or silently skipping it.
- **Short caption draft**, for short-form entries: a complete, ready-to-post caption, not just the hook
- **Long-form angle**, for long-form entries: a one to two sentence description of the argument or story, plus a suggested title. Flag it "ready to draft" rather than writing the full body here, point the user to `social-copywriting` when they're ready to produce it in full
- **Visual note**: a short line on what kind of visual would pair with this post (defer to `visual-direction` for a fuller recommendation if that skill is active)

## Platform interchangeability rule

Platforms sharing the same format classification (short-form or long-form) are treated as interchangeable slots, the same hook/caption or angle/title can serve either, unless the user wants platform-specific variants. Only produce distinct variants for each platform in a pair if the user explicitly asks for platform-specific nuance. Otherwise, one draft per format type per calendar slot is enough, labeled with which platforms it could serve.

## Output format

- **Default**: present the calendar inline as a markdown table. Fast to scan, easy to revise conversationally.
- **File output**: produce an actual downloadable file instead of (or in addition to) the inline table when the user asks to save, download, export, or share it, or when the timeframe is long enough (roughly a month or more, or a high posting cadence) that a table in chat would be unwieldy. Default to a spreadsheet for anything the user will likely update or check off over time; use a document only if they specifically want a written/narrative version.
- If unsure which the user wants, default to the inline table and mention a downloadable version is available on request.

## Revising the calendar

Treat the calendar as a living draft. If the user asks to swap a topic, move a date, change a platform, or regenerate one entry, edit just that entry rather than regenerating the whole calendar, unless they ask for a full redo.
