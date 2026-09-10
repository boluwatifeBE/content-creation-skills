---
name: fashion-case-study-builder
description: Turns a completed fashion design project or collection into a structured case study post (concept, development, execution, result), built for portfolio and lead-generation content. Use whenever the user wants to write up a finished project or collection, turn client or personal work into a case study, or asks to "showcase," "document," or "write up" a project they completed. Requires creator-context to be active. This is a field-specific pack skill for Fashion, if the user's stated persona doesn't include fashion design or a clear equivalent, flag a soft warning before proceeding. Distinct from fashion-asset-to-content (a single lesson mined from one asset) since a case study follows a full project narrative arc.
---

# Fashion Case Study Builder

Field pack skill for **Fashion**. Turns a completed design project or collection into a structured case study, following the concept-to-execution arc that makes a fashion case study credible, rather than jumping straight from inspiration to finished garment.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include fashion design or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Confidentiality check (before gathering anything else)

Ask directly: can the client or collection be named, or does this need to stay anonymized? Client commissions and unreleased or pre-launch collections often carry confidentiality obligations.

- If it can be named, proceed normally.
- If it needs to be anonymized, or the user is unsure how much detail is safe to share, hand off to `fashion-confidential-story` for the anonymization work, then return here once the sanitized version of events is confirmed.

## Draft-or-generate checkpoint

Ask whether the user has notes, sketches, or a project summary already written up, or wants help structuring the case study from a description they give now. Work from whatever they have rather than assuming a blank start.

## Gathering the project

Ask for, or extract from what's given:

- **The concept/brief**: what problem, brief, or creative idea started this project, for a client commission or personal collection
- **The development**: the actual process, textile sourcing, silhouette development, sampling and fitting iterations, this is often the most interesting and most compressed part, don't let the case study jump from concept straight to finished piece without naming what actually happened in between, the fittings that didn't work, the fabric that got swapped, the construction problem that had to be solved
- **The execution**: what was actually built or delivered, specific enough to be credible
- **The result**: how it was received, worn, shown, or sold, real feedback, press, or outcomes if the user has them. Never invent a result the user didn't provide, if there's no clear outcome yet, say the project is recent or the reception isn't yet known, rather than fabricating a plausible-sounding response.

## Structuring the case study

Build the piece around the arc: Concept, Development, Execution, Result, in that order, since skipping the development stage is the most common way fashion case studies read as a portfolio showcase rather than a genuine process story. A closing reflection (what this project taught, or what it reinforced about the user's approach) is optional but often strengthens the piece.

## Format

Case studies generally need more room than a standard short-form post, default to treating this as a **long-form piece** (per the user's long-form platform classification), unless the user specifically wants a short-form teaser version too, in which case produce a short highlight that points toward the fuller story rather than compressing the whole arc into a caption.

## House style and voice

Apply the confirmed house style. Case studies can tolerate slightly more structure (subheadings for each arc stage) than other long-form content, since the reader benefits from seeing the shape of the story, but keep prose within each section following the same voice and formatting principles as everything else in this system.

## Visual note

Ask what visual material exists (sketches, fitting photos, final garment shots, show or shoot images) and recommend which would strengthen the piece, defer to `visual-direction` for a fuller recommendation if that skill is active.

## Carousel option

A case study's arc maps unusually well onto a carousel, each stage of the arc can become one or two slides. Ask the user if they'd rather present this case study as a carousel instead of (or alongside) the long-form piece, and if so, hand off to `social-copywriting`'s carousel structure, one slide per arc stage, rather than building slides here.

## Presenting the output

Present the case study clearly labeled by arc stage or with clear section breaks. If any stage is thin (a vague development process, an unmeasured result), say so honestly rather than padding it, a case study missing a real development story or a real result is weaker for the reader even if it's longer.
