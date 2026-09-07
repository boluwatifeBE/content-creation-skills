---
name: ux-asset-to-content
description: Field pack skill for UX/Product Research and Design, including UX engineering, design-to-code, and AI-assisted design workflows. Turns an uploaded UX or research asset (wireframe, user flow, prototype screenshot, research report excerpt, usability test finding, information architecture map, design system component) into a small set of publish-ready social posts by identifying what the asset structurally represents and the real human or business problem it solves, then mining that into a lesson-driven post. Use whenever the user uploads a UX-related asset alongside a request to turn it into content, post about it, extract a lesson from it, or asks "what can I post about this." Requires creator-context to be active first. This is a field-specific pack skill, if the user's stated persona doesn't include UX, product research, product design, or UX engineering, flag a soft warning before proceeding.
---

# UX Asset to Content

Field pack skill for **UX/Product Research and Design**, covering research, information architecture, interaction and UI design, UX engineering, vibe coding, AI-assisted design workflows, and design-to-code.

Takes a single uploaded UX-related asset plus a directional prompt and turns it into a small, ready-to-post content series, grounded in what the asset actually is and the real problem it demonstrates. This is the skill for "I have this artifact from my work, help me post about it," not for writing from a topic the user already has in mind (that's `social-copywriting`), and not for generating fresh topic ideas without a source asset (that's `ux-content-ideation`).

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include UX, product research, product design, UX engineering, or a clear equivalent. If yes, proceed silently. If no, or if `creator-context` hasn't captured a field at all, surface a soft warning: *"This skill is built for UX and product research/design work, your stated field doesn't clearly match, want to proceed anyway, or is this the wrong pack for what you're working on?"* Proceed based on their answer, this is a warning, not a block.

## Before starting

Confirm `creator-context` is active beyond just the field check, persona, philosophy, house style, and profile all need to be established.

Check for an actual uploaded file. A description of an asset in the user's message is not the same as an uploaded file, if they've referenced something without attaching it, ask them to upload it before proceeding rather than working from assumptions about what it contains.

## Step 1: Read the asset

Use the appropriate file-reading approach for the asset type (image, PDF, document, or text/data file) to actually see or read its content before doing anything else. Don't generate content from the filename or the user's brief description alone.

## Step 2: Identify what the asset structurally represents

Name, specifically, what kind of artifact this is: a wireframe, a high-fidelity prototype screenshot, a user flow or journey map, an information architecture diagram, a research report excerpt, a usability test finding, a persona document, a design system component or token sheet, a design-to-code handoff spec, or an AI-generated design/prototype from a vibe-coding workflow. This framing matters because the lesson a post draws should come from the artifact's actual function in the process, not a generic reaction to it.

State this identification back to the user in one line before moving on, so a misread gets caught immediately.

## Step 3: Propose directions and check before going deeper (required checkpoint)

Do not proceed to analyzing the underlying problem or writing copy until this step is complete.

Propose 2 to 3 distinct, concrete directions grounded in real UX content formats, for example:
- **Process/decision walkthrough**: how a specific design or research decision got made, and why, tracing the reasoning a viewer wouldn't see just by looking at the final artifact
- **Research-to-design translation**: how a specific finding (from testing, interviews, analytics) actually shaped a design decision, connecting the research artifact to its consequence
- **Craft teardown**: picking one or two specific interaction or structural choices and explaining what problem they solve
- **Workflow/tool spotlight**: if the asset came from an AI-assisted or vibe-coding workflow, focusing the post on the workflow itself, what the tool did well, what still needed human judgment, rather than only the resulting artifact

Ask the user which direction fits, or invite them to describe their own. If the user already gave a directional prompt when uploading, treat that as their answer, confirm your understanding of it in one line, and still ask what specific emphasis they want within that direction before writing.

Do not draft any copy until the user has confirmed a direction.

## Step 4: Identify the underlying problem, within the confirmed direction

Ask, and answer for yourself before writing anything: what human or business problem does this asset actually solve, or fail to solve, in the context of the chosen direction? Consider, where relevant to what's visible: cognitive load, task completion friction, information findability, accessibility, trust signals, or the specific behavioral pattern the research or design choice responds to.

Push for the specific, non-obvious insight, the kind of observation that only someone who's actually done dozens of these would notice.

**Do not assign a research finding, user behavior claim, or usability outcome to the asset unless the user has confirmed it, or it's directly visible in provided research data.** If a claim about why users behave a certain way or how they responded isn't confirmed, ask about it directly rather than asserting it. This is a stricter version of the same discipline used elsewhere in this system, because unconfirmed behavioral claims in UX content are especially easy to overstate as if they were real findings.

## Step 5: Generate the content

Produce a post that details a specific, real-world lesson inspired directly by the asset and grounded in what was actually confirmed in steps 3 and 4, not invented.

Follow the platform-pairing rule used across this system: one **short-form draft** and one **long-form draft**, per the user's platform format classifications in `creator-context`. Only produce platform-specific variants if the user explicitly asks for that nuance.

## Step 6: Recommend a visual

Recommend a visual to pair with the content: the asset itself (cropped, annotated, or presented as-is), a derived visual (a simplified flow diagram, a before/after), or something new entirely. Hand off to `visual-direction` for a fuller recommendation if that skill is active, otherwise give a short, concrete suggestion inline.

## Presenting the output

Present both drafts as plain text, ready to copy and paste, clearly labeled by which platform pair each is for. Lead with a one or two sentence summary of what the asset is and the lesson pulled from it, so the user can sanity-check the read before scanning the full drafts.

## A note on pacing

This skill has two points where it must stop and wait for the user rather than pushing through to a finished post: the direction checkpoint in step 3, and any behavioral-claim confirmation in step 4. A fast, confident-sounding post that skips these checks isn't a better outcome, it's a worse one.
