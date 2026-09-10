---
name: marketing-case-study-builder
description: Turns a completed marketing campaign or client project into a structured case study post (challenge, strategy, execution, result), built for portfolio and lead-generation content. Use whenever the user wants to write up a finished campaign or project, turn client work into a case study, or asks to "showcase," "document," or "write up" a project they completed. Requires creator-context to be active. This is a field-specific pack skill for Business Marketing, if the user's stated persona doesn't include marketing or a clear equivalent, flag a soft warning before proceeding. Distinct from marketing-asset-to-content (a single lesson mined from one asset) since a case study follows a full project narrative arc.
---

# Marketing Case Study Builder

Field pack skill for **Business Marketing**. Turns a completed campaign or project into a structured case study, built around the Challenge/Strategy/Execution/Result arc marketing case studies are expected to follow. This is the skill in this pack where the metrics discipline matters most, marketing case studies are expected to show numbers, which makes fabricating an impressive one especially tempting and especially damaging if it isn't true.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include marketing, growth marketing, digital marketing, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Confidentiality check (before gathering anything else)

Ask directly: can the client or campaign be named, or does this need to stay anonymized? Marketing case studies often involve budget figures, revenue numbers, or strategic details clients don't want public even after a project ends.

- If it can be named, proceed normally.
- If it needs to be anonymized, or the user is unsure how much detail is safe to share, hand off to `marketing-confidential-story` for the anonymization work, then return here once the sanitized version of events is confirmed.

## Draft-or-generate checkpoint

Ask whether the user has notes, a campaign report, or a project summary already written up, or wants help structuring the case study from a description they give now. Work from whatever they have rather than assuming a blank start.

## Gathering the project

Ask for, or extract from what's given:

- **The challenge**: what problem or brief existed, what wasn't working before this campaign, for the client or the business
- **The strategy**: what approach was chosen and why, the actual reasoning, not just "we ran ads," what specific insight or constraint shaped the strategic direction
- **The execution**: what was actually done, specific channels, creative approach, targeting, sequencing, specific enough to be credible
- **The result**: real outcomes, only what the user actually has and can stand behind. Never invent a metric, a percentage, or a dollar figure that wasn't provided. If the result is genuinely strong, use the real number. If it's modest, use the real modest number rather than a more impressive invented one. If there's no measured result yet, say so plainly rather than fabricating a plausible-sounding figure.

## Structuring the case study

Build the piece around the arc: Challenge, Strategy, Execution, Result, in that order. The strategy step is what separates a case study from a project recap, make sure the reasoning behind the approach is explicit, not just a list of tactics. A closing reflection (what this project taught, or what it reinforced about the user's approach) is optional but often strengthens the piece.

## A specific caution on rounding and framing numbers

Even with real numbers, framing can mislead. Don't select the single most flattering metric while omitting context that would change how it reads (a large percentage increase off a tiny base, a short measurement window, cherry-picked timeframe). If the user provides a metric that needs context to be honestly represented, include that context rather than presenting the number in isolation for maximum impact.

## Format

Case studies generally need more room than a standard short-form post, default to treating this as a **long-form piece** (per the user's long-form platform classification), unless the user specifically wants a short-form teaser version too, in which case produce a short highlight that points toward the fuller story rather than compressing the whole arc into a caption.

## House style and voice

Apply the confirmed house style. Case studies can tolerate slightly more structure (subheadings for each arc stage) than other long-form content, since the reader benefits from seeing the shape of the story, but keep prose within each section following the same voice and formatting principles as everything else in this system.

## Visual note

Ask what visual material exists (before/after performance charts, creative samples, funnel diagrams) and recommend which would strengthen the piece, defer to `visual-direction` for a fuller recommendation if that skill is active.

## Carousel option

A case study's arc maps unusually well onto a carousel, each stage of the arc can become one or two slides. Ask the user if they'd rather present this case study as a carousel instead of (or alongside) the long-form piece, and if so, hand off to `social-copywriting`'s carousel structure, one slide per arc stage, rather than building slides here.

## Presenting the output

Present the case study clearly labeled by arc stage or with clear section breaks. If any stage is thin (a vague strategy, an unmeasured result), say so honestly rather than padding it, a case study missing real strategic reasoning or a real result is weaker for the reader even if it's longer.
