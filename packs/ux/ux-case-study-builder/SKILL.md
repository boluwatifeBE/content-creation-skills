---
name: ux-case-study-builder
description: Turns a completed UX or product research project into a structured case study post (challenge, research/insight, design decision, validation/result), built for portfolio and lead-generation content. Use whenever the user wants to write up a finished project, turn client or in-house work into a case study, or asks to "showcase," "document," or "write up" a project they completed. Requires creator-context to be active. This is a field-specific pack skill for UX/Product Research and Design, if the user's stated persona doesn't include either, flag a soft warning before proceeding. Distinct from ux-asset-to-content (a single lesson mined from one asset) since a case study follows a full project narrative arc.
---

# UX Case Study Builder

Field pack skill for **UX/Product Research and Design**. Turns a completed project into a structured case study, following the research-to-design arc that makes UX case studies credible, rather than jumping straight from problem to pretty solution.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include UX, product research, product design, UX engineering, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Confidentiality check (before gathering anything else)

Ask directly: can the client or product be named, or does this need to stay anonymized? Client and in-house product work often carries confidentiality obligations, especially for unreleased features or competitive-sensitive products.

- If it can be named, proceed normally.
- If it needs to be anonymized, or the user is unsure how much detail is safe to share, hand off to `ux-confidential-story` for the anonymization work, then return here once the sanitized version of events is confirmed.

## Draft-or-generate checkpoint

Ask whether the user has notes, a research report, or a project summary already written up, or wants help structuring the case study from a description they give now. Work from whatever they have rather than assuming a blank start.

## Gathering the project

Ask for, or extract from what's given:

- **The challenge**: what problem or brief existed, what wasn't working before this project, for the user or the business
- **The research and insight**: what method was used (interviews, usability testing, analytics, surveys), and what was actually found, this is the step most likely to get compressed or skipped, don't let the case study jump from challenge straight to a design solution without naming what the research actually revealed
- **The design decision**: what was actually built or changed, specific enough to be credible, connected explicitly back to the research finding that motivated it, not just "we redesigned it to be cleaner"
- **The validation/result**: how the change was tested or measured afterward, usability testing results, adoption or completion rate changes, qualitative feedback, whatever the user actually has. Never invent a metric or outcome the user didn't provide, if there's no clear result yet or it hasn't been measured, say so plainly rather than fabricating a plausible-sounding number.

## Structuring the case study

Build the piece around the arc: Challenge, Research/Insight, Design Decision, Validation/Result, in that order. The research-to-decision link is the part that most differentiates a credible UX case study from a portfolio piece that just shows pretty screens, make that connection explicit rather than implied. A closing reflection (what this project taught, or what it reinforced about the user's approach to research or design) is optional but often strengthens the piece.

## Format

Case studies generally need more room than a standard short-form post, default to treating this as a **long-form piece** (per the user's long-form platform classification), unless the user specifically wants a short-form teaser version too, in which case produce a short highlight that points toward the fuller story rather than compressing the whole arc into a caption.

## House style and voice

Apply the confirmed house style. Case studies can tolerate slightly more structure (subheadings for each arc stage) than other long-form content, since the reader benefits from seeing the shape of the story, but keep prose within each section following the same voice and formatting principles as everything else in this system.

## Visual note

Ask what visual material exists (before/after screens, flow diagrams, testing footage or notes) and recommend which would strengthen the piece, defer to `visual-direction` for a fuller recommendation if that skill is active.

## Presenting the output

Present the case study clearly labeled by arc stage or with clear section breaks. If any stage is thin (research that didn't really inform the decision, an unmeasured result), say so honestly rather than padding it, a case study missing a real research-to-decision link or a real result is weaker for the reader even if it's longer.
