---
name: marketing-asset-to-content
description: Field pack skill for Business Marketing, spanning paid advertising, email, SEO, content marketing, and marketing strategy. Turns an uploaded marketing asset (a campaign report, an ad creative, an email sequence, a funnel diagram, an analytics dashboard, a landing page screenshot) into a small set of publish-ready social posts by identifying what the asset structurally represents and the real business problem it solves, then mining that into a lesson-driven post. Use whenever the user uploads a marketing-related asset alongside a request to turn it into content, post about it, extract a lesson from it, or asks "what can I post about this." Requires creator-context to be active first. This is a field-specific pack skill, if the user's stated persona doesn't include marketing, growth, or a clear equivalent, flag a soft warning before proceeding.
---

# Marketing Asset to Content

Field pack skill for **Business Marketing**, spanning paid advertising, email, SEO, content marketing, and marketing strategy generally, not scoped to one channel.

Takes a single uploaded marketing-related asset plus a directional prompt and turns it into a small, ready-to-post content series, grounded in what the asset actually is and the real problem it demonstrates. This is the skill for "I have this marketing artifact, help me post about it," not for writing from a topic the user already has in mind (that's `social-copywriting`), and not for generating fresh topic ideas without a source asset (that's `marketing-content-ideation`).

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include marketing, growth marketing, digital marketing, or a clear equivalent. If yes, proceed silently. If no, or if `creator-context` hasn't captured a field at all, surface a soft warning: *"This skill is built for marketing work, your stated field doesn't clearly match, want to proceed anyway, or is this the wrong pack for what you're working on?"* Proceed based on their answer, this is a warning, not a block.

## Before starting

Confirm `creator-context` is active beyond just the field check, persona, philosophy, house style, and profile all need to be established.

Check for an actual uploaded file. A description of an asset in the user's message is not the same as an uploaded file, if they've referenced something without attaching it, ask them to upload it before proceeding rather than working from assumptions about what it contains.

## Step 1: Read the asset

Use the appropriate file-reading approach for the asset type (image, PDF, document, or data file) to actually see or read its content before doing anything else. Don't generate content from the filename or the user's brief description alone.

## Step 2: Identify what the asset structurally represents

Name, specifically, what kind of artifact this is: a campaign performance report, an ad creative or ad set, an email sequence, a funnel or customer journey diagram, an analytics dashboard, a landing page, an SEO audit, a content calendar or editorial plan, or a positioning/strategy document. This framing matters because the lesson a post draws should come from the artifact's actual function, not a generic reaction to it.

State this identification back to the user in one line before moving on, so a misread gets caught immediately.

## Step 3: Propose directions and check before going deeper (required checkpoint)

Do not proceed to analyzing the underlying problem or writing copy until this step is complete.

Propose 2 to 3 distinct, concrete directions grounded in real marketing content formats, for example:
- **Strategy walkthrough**: how a specific decision (channel choice, targeting, offer structure) connects to the underlying business goal
- **Process/decision teardown**: picking one or two specific choices (a subject line, a CTA, an audience segment) and explaining the reasoning behind them
- **Results-and-lesson framing**: if real performance data exists, what happened and what it reveals, handled with the strict metrics discipline in Step 4
- **Mistake/lesson-learned framing**: what didn't work and what that revealed, often more valuable and more credible than only-success content

Ask the user which direction fits, or invite them to describe their own. If the user already gave a directional prompt when uploading, treat that as their answer, confirm your understanding of it in one line, and still ask what specific emphasis they want within that direction before writing.

Do not draft any copy until the user has confirmed a direction.

## Step 4: Identify the underlying problem, within the confirmed direction, with strict metrics discipline

Ask, and answer for yourself before writing anything: what business problem does this asset actually address, acquisition, retention, awareness, conversion, cost efficiency? Push for the specific, non-obvious insight, not a generic observation.

**Never state or imply a performance number, result, or outcome that wasn't actually provided in the asset or confirmed by the user.** Marketing content has a strong pull toward impressive-sounding numbers, resist it entirely. If the asset shows a real metric, use it accurately. If it doesn't, don't invent one, don't round favorably, and don't imply a result wasn't measured. If the direction is results-based but no real data exists, say so and suggest a different direction instead.

**Do not assign strategic intent or a causal explanation to a choice unless the user has confirmed it.** If it's not obvious why a specific decision was made, ask rather than guessing at the reasoning and presenting the guess as fact.

## Step 5: Generate the content

Produce a post that details a specific, real-world lesson inspired directly by the asset and grounded in what was actually confirmed in steps 3 and 4, not invented.

Follow the platform-pairing rule used across this system: one **short-form draft** and one **long-form draft**, per the user's platform format classifications in `creator-context`. Only produce platform-specific variants if the user explicitly asks for that nuance.

## Step 6: Recommend a visual

Recommend a visual to pair with the content: the asset itself (cropped, annotated, or presented as-is, with any sensitive figures redacted if needed), a derived visual (a simplified chart), or something new entirely. Hand off to `visual-direction` for a fuller recommendation if that skill is active, otherwise give a short, concrete suggestion inline.

## Carousel option

This content type often works well as a carousel too, a single asset naturally breaks into a title slide, a few points about what it shows, and a lesson slide. Ask the user if they'd rather have this as a carousel instead of (or alongside) the two-draft output, and if so, hand off to `social-copywriting`'s carousel structure rather than building slides here.

## Presenting the output

Present both drafts as plain text, ready to copy and paste, clearly labeled by which platform pair each is for. Lead with a one or two sentence summary of what the asset is and the lesson pulled from it, so the user can sanity-check the read before scanning the full drafts.

## A note on pacing

This skill has two points where it must stop and wait for the user rather than pushing through to a finished post: the direction checkpoint in step 3, and any metric or intent confirmation in step 4. A fast, confident-sounding post that skips these checks isn't a better outcome, it's a worse one, especially where a fabricated or exaggerated metric is involved.
