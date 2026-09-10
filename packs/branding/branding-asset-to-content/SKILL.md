---
name: branding-asset-to-content
description: Field pack skill for Brand Identity Design and Brand Strategy. Turns an uploaded brand asset (logo grid, brand identity presentation, mood board, style guide, packaging mockup, pitch deck slide, wireframe, or similar) into a small set of publish-ready social posts by identifying what the asset structurally represents and the real human or business problem it solves, then mining that into a lesson-driven post. Use whenever the user uploads a brand-related asset alongside a request to turn it into content, post about it, extract a lesson from it, or asks "what can I post about this." Requires creator-context to be active first. This is a field-specific pack skill, if the user's stated persona in creator-context doesn't include brand identity design or brand strategy, flag a soft warning before proceeding.
---

# Branding Asset to Content

Field pack skill for **Brand Identity Design and Brand Strategy**, treated as one combined field pack since they're rarely separable in real practice, a mark can't be defended without the positioning underneath it.

Takes a single uploaded brand-related asset plus a directional prompt and turns it into a small, ready-to-post content series, grounded in what the asset actually is and the real problem it demonstrates. This is the skill for "I have this brand asset, help me post about it," not for writing from a topic the user already has in mind (that's `social-copywriting`), and not for generating fresh topic ideas without a source asset (that's `branding-content-ideation`).

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include brand identity design, brand strategy, or a clear equivalent (brand designer, brand consultant, identity designer, and similar). If yes, proceed silently. If no, or if `creator-context` hasn't captured a field at all, surface a soft warning: *"This skill is built for brand identity and brand strategy work, your stated field doesn't clearly match, want to proceed anyway, or is this the wrong pack for what you're working on?"* Proceed based on their answer, this is a warning, not a block.

## Before starting

Confirm `creator-context` is active beyond just the field check, persona, philosophy, house style, and profile all need to be established.

Check for an actual uploaded file. A description of an asset in the user's message is not the same as an uploaded file, if they've referenced something without attaching it, ask them to upload it before proceeding rather than working from assumptions about what it contains.

## Step 1: Read the asset

Use the appropriate file-reading approach for the asset type (image, PDF, document, vector, or brief/text file) to actually see or read its content before doing anything else. Don't generate content from the filename or the user's brief description alone.

## Step 2: Identify what the asset structurally represents

Name, specifically, what kind of brand artifact this is: a logo grid, a brand identity presentation, a mood board, a style guide or brand guidelines document, a packaging mockup, a pitch deck slide, a wireframe, a naming exploration, a competitive positioning map, a tone-of-voice document, or similar. This framing matters because the lesson a post draws should come from the artifact's actual function within brand strategy or identity work, not a generic reaction to it.

State this identification back to the user in one line before moving on, so a misread gets caught immediately.

## Step 3: Propose directions and check before going deeper (required checkpoint)

Do not proceed to analyzing the underlying problem or writing copy until this step is complete. This is the step that most determines whether the final post feels earned or generic.

Propose 2 to 3 distinct, concrete directions grounded in real branding content formats, for example:
- **Brand story**: how the identity or strategy choices connect to the business's actual goals, positioning, or mission (the "how we got here" format)
- **Presentation-style reveal**: a confident "here's the finished system" walkthrough, similar to how studios like Koto or Pentagram unveil a rebrand
- **Process/decision teardown**: picking one or two specific choices (a mark, a color system, a positioning statement) and explaining the strategic or design logic behind them
- **Strategy-first framing**: leading with the underlying strategic problem (differentiation, brand architecture, audience perception) and showing the visual/identity work as the resolution to it

Ask the user which direction fits, or invite them to describe their own. If the user already gave a directional prompt when uploading, treat that as their answer, confirm your understanding of it in one line, and still ask what specific emphasis they want within that direction before writing.

Do not draft any copy until the user has confirmed a direction.

## Step 4: Identify the underlying problem, within the confirmed direction

Ask, and answer for yourself before writing anything: what human or business problem does this asset actually solve, or fail to solve, in the context of the chosen direction? Consider, where relevant to what's visible in the asset: positioning and differentiation, brand architecture, audience perception, tone of voice, competitive context, or the functional job the identity system has to do (scale across applications, signal trust, feel approachable, and so on).

Push for the specific, non-obvious insight, the kind of observation that only someone who's actually built or reviewed dozens of these would notice.

**Do not assign meaning to a specific visual element (a color, an object, a prop, a photo choice) unless the user has confirmed that meaning, or it's a well-established convention.** If a detail looks intentional or symbolic but hasn't been confirmed, ask about it directly rather than building a claim on top of a guess. Getting this wrong undermines the credibility of the whole post.

## Step 5: Generate the content

Produce a post that details a specific, real-world lesson inspired directly by the asset and grounded in what was actually confirmed in steps 3 and 4, not invented.

Follow the platform-pairing rule used across this system: one **short-form draft** and one **long-form draft**, per the user's platform format classifications in `creator-context`. Only produce platform-specific variants if the user explicitly asks for that nuance.

## Step 6: Recommend a visual

Recommend a visual to pair with the content: the asset itself (cropped, annotated, or presented as-is), a derived visual, or something new entirely. Hand off to `visual-direction` for a fuller recommendation if that skill is active, otherwise give a short, concrete suggestion inline.

## Carousel option

This content type often works well as a carousel too, a single asset naturally breaks into a title slide, a few points about what it shows, and a lesson slide. Ask the user if they'd rather have this as a carousel instead of (or alongside) the two-draft output, and if so, hand off to `social-copywriting`'s carousel structure rather than building slides here.

## Presenting the output

Present both drafts as plain text, ready to copy and paste, clearly labeled by which platform pair each is for. Lead with a one or two sentence summary of what the asset is and the lesson pulled from it, so the user can sanity-check the read before scanning the full drafts.

## A note on pacing

This skill has two points where it must stop and wait for the user rather than pushing through to a finished post: the direction checkpoint in step 3, and any element-meaning confirmation in step 4. A fast, confident-sounding post that skips these checks isn't a better outcome, it's a worse one.
