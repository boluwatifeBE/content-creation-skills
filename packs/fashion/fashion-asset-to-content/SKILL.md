---
name: fashion-asset-to-content
description: Field pack skill for Fashion, spanning fashion design, fashion blogging/styling, and the fashion industry generally. Turns an uploaded fashion asset (a sketch, a mood board, a tech pack, a lookbook, a fabric swatch board, a runway photo, or an outfit/look photo) into a small set of publish-ready social posts by identifying what the asset structurally represents and the real creative or business problem it solves, then mining that into a lesson-driven post. Use whenever the user uploads a fashion-related asset alongside a request to turn it into content, post about it, extract a lesson from it, or asks "what can I post about this." Requires creator-context to be active first. This is a field-specific pack skill, if the user's stated persona doesn't include fashion design, fashion blogging/styling, or a clear equivalent, flag a soft warning before proceeding.
---

# Fashion Asset to Content

Field pack skill for **Fashion**, spanning fashion design, fashion blogging and styling, and the fashion industry generally. Because this pack covers both design craft and personal styling content, this skill deliberately handles a wider range of asset types than most other packs' asset-to-content skills, from a technical tech pack to a single outfit photo.

Takes a single uploaded fashion-related asset plus a directional prompt and turns it into a small, ready-to-post content series, grounded in what the asset actually is and the real problem it demonstrates. This is the skill for "I have this fashion asset, help me post about it," not for writing from a topic the user already has in mind (that's `social-copywriting`), and not for generating fresh topic ideas without a source asset (that's `fashion-content-ideation`).

## Field match check (required first step)

Before anything else, check whether the user's stated field(s) in `creator-context` include fashion design, fashion blogging, styling, or a clear equivalent. If yes, proceed silently. If no, or if `creator-context` hasn't captured a field at all, surface a soft warning: *"This skill is built for fashion design and styling work, your stated field doesn't clearly match, want to proceed anyway, or is this the wrong pack for what you're working on?"* Proceed based on their answer, this is a warning, not a block.

## Before starting

Confirm `creator-context` is active beyond just the field check, persona, philosophy, house style, and profile all need to be established.

Check for an actual uploaded file. A description of an asset in the user's message is not the same as an uploaded file, if they've referenced something without attaching it, ask them to upload it before proceeding rather than working from assumptions about what it contains.

## Step 1: Read the asset

Use the appropriate file-reading approach for the asset type (image or document) to actually see or read its content before doing anything else. Don't generate content from the filename or the user's brief description alone.

## Step 2: Identify what the asset structurally represents

Name, specifically, what kind of artifact this is: a design sketch or croquis, a mood board, a technical/spec pack, a fabric swatch or textile board, a lookbook or collection lineup, a runway or show photo, a fitting/sampling photo, or an outfit/look photo assembled for styling content. This framing matters because the lesson a post draws should come from the artifact's actual function, whether that's a design decision, a construction choice, or a styling principle, not a generic reaction to it.

State this identification back to the user in one line before moving on, so a misread gets caught immediately.

## Step 3: Propose directions and check before going deeper (required checkpoint)

Do not proceed to analyzing the underlying problem or writing copy until this step is complete.

Propose 2 to 3 distinct, concrete directions grounded in real fashion content formats, for example:
- **Design/construction walkthrough**: how a specific design or construction choice (a silhouette, a textile pairing, a finishing detail) connects to the garment's function or the collection's concept
- **Styling breakdown**: for an outfit or look, why the pieces work together, proportion, color, silhouette balance, occasion fit
- **Process story**: the development arc of a piece or collection, from concept through iteration
- **Trend or industry commentary**: if the asset connects to a broader pattern in the industry (a construction technique gaining traction, a shift in silhouette trends), framing the post around that wider context

Ask the user which direction fits, or invite them to describe their own. If the user already gave a directional prompt when uploading, treat that as their answer, confirm your understanding of it in one line, and still ask what specific emphasis they want within that direction before writing.

Do not draft any copy until the user has confirmed a direction.

## Step 4: Identify the underlying problem, within the confirmed direction

Ask, and answer for yourself before writing anything: what creative or business problem does this asset actually solve? Depending on the direction, this might be a construction problem (how to achieve a silhouette within fabric constraints), a styling problem (how to make disparate pieces read as intentional), or a business problem (how a collection needs to balance creative vision against production cost or market fit).

Push for the specific, non-obvious insight, the kind of observation that only someone who's actually done dozens of these would notice.

**Do not assign meaning, intent, or inspiration to a specific design choice (a color, a silhouette, a fabric, a detail) unless the user has confirmed it.** If a choice looks intentional or symbolic but hasn't been confirmed, ask about it directly rather than building a claim on top of a guess. Getting this wrong undermines the credibility of the whole post.

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

This skill has two points where it must stop and wait for the user rather than pushing through to a finished post: the direction checkpoint in step 3, and any intent/meaning confirmation in step 4. A fast, confident-sounding post that skips these checks isn't a better outcome, it's a worse one.
