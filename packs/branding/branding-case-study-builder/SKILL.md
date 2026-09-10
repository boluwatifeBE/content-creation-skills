---
name: branding-case-study-builder
description: Turns a completed brand identity or brand strategy project into a structured case study post (challenge, insight, approach, result), built for portfolio and lead-generation content. Use whenever the user wants to write up a finished project, turn client work into a case study, or asks to "showcase," "document," or "write up" a project they completed. Requires creator-context to be active. This is a field-specific pack skill for Brand Identity Design and Brand Strategy, if the user's stated persona doesn't include either, flag a soft warning before proceeding. Distinct from branding-asset-to-content (a single lesson mined from one asset) since a case study follows a full project narrative arc.
---

# Branding Case Study Builder

Field pack skill for **Brand Identity Design and Brand Strategy**. Turns a completed project into a structured case study, a genuinely different narrative shape than a single-lesson post, built specifically to serve portfolio and lead-generation goals.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include brand identity design, brand strategy, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Confidentiality check (before gathering anything else)

Ask directly: can the client be named, or does this need to stay anonymized? Client work often carries confidentiality obligations that don't disappear just because the project is finished.

- If the client can be named, proceed normally.
- If it needs to be anonymized, or the user is unsure how much detail is safe to share, hand off to `branding-confidential-story` for the anonymization work, then return here once the sanitized version of events is confirmed, don't attempt heavy anonymization within this skill, that's a distinct, more careful task with its own skill.

## Draft-or-generate checkpoint

Ask whether the user has notes, a brief, or a project summary already written up, or wants help structuring the case study from a description they give now. Work from whatever they have rather than assuming a blank start.

## Gathering the project

Ask for, or extract from what's given:

- **The challenge**: what problem or brief did the client bring, what wasn't working before this project
- **The insight**: what did the strategic or research work uncover that shaped the direction, this is often the most interesting and most skipped part, don't let the case study jump straight from challenge to solution without naming what was actually learned in between
- **The approach**: what was actually done, the identity system, the positioning work, the process, specific enough to be credible, not just "we did research and design"
- **The result**: what happened after, qualitative (how the client or market responded) or quantitative (real metrics) if the user has them. Never invent a result or a number the user didn't provide, if there's no clear outcome yet or the user doesn't have data, say the project is recent or the impact isn't yet measured, rather than fabricating a plausible-sounding result.

## Structuring the case study

Build the piece around the arc: Challenge, Insight, Approach, Result, in that order, since skipping the insight step is the most common way case studies read as a portfolio piece rather than a strategic story. A closing reflection or lesson (what this project taught, or what it reinforced about how the user approaches this kind of work) is optional but often strengthens the piece, connecting it back to the user's broader philosophy from `creator-context`.

## Format

Case studies generally need more room than a standard short-form post, default to treating this as a **long-form piece** (per the user's long-form platform classification), unless the user specifically wants a short-form teaser version too, in which case produce a short highlight that points toward the fuller story rather than trying to compress the whole arc into a caption.

## House style and voice

Apply the confirmed house style. Case studies can tolerate slightly more structure (subheadings for each arc stage) than other long-form content, since the reader benefits from being able to see the shape of the story, but keep prose within each section following the same voice and formatting principles as everything else in this system.

## Visual note

Ask what visual material exists (before/after shots, process documentation, final applications) and recommend which would strengthen the piece, defer to `visual-direction` for a fuller recommendation if that skill is active.

## Carousel option

A case study's arc maps unusually well onto a carousel, each stage of the arc can become one or two slides. Ask the user if they'd rather present this case study as a carousel instead of (or alongside) the long-form piece, and if so, hand off to `social-copywriting`'s carousel structure, one slide per arc stage, rather than building slides here.

## Presenting the output

Present the case study clearly labeled by arc stage or with clear section breaks, so the user can see the structure at a glance. If any stage is thin (a weak insight, an unclear result), say so honestly rather than padding it, a case study missing a real insight or result is weaker for the reader even if it's longer.
