---
name: content-repurposing
description: Transforms an existing piece of content, the user's own draft, a past post, or something social-copywriting produced earlier, from one format to another, compressing a long-form piece into a short-form post, or expanding a short-form post into a full long-form piece. Use whenever the user asks to "repurpose," "turn this into a," "shorten this for," "expand this into," "make a thread/post out of this article," or wants one piece of content adapted for a different platform or length than it was originally written for. Requires creator-context to be active for house style and platform format classifications. Distinct from social-copywriting (which writes new copy from a topic) and asset-to-content (which mines a non-text asset like an image or PDF for a topic).
---

# Content Repurposing

Takes a piece of content that already exists and reshapes it for a different format, compressing long-form into short-form, or expanding short-form into long-form. The source material is always something the user already has, this skill never invents new subject matter, it transforms what's already there.

## Before starting

Confirm `creator-context` is active for house style and platform format classifications. If not established, capture the essentials first.

Get the source content directly, pasted text, an uploaded file, or a reference to something already produced earlier in this conversation (e.g. "the LinkedIn post you wrote for me on Monday"). Don't work from a description of the content, get the actual text.

## Establishing the transformation

Confirm, if not already clear:

- **Direction**: compress (long-form to short-form) or expand (short-form to long-form)
- **Target platform or format**: pulled from the user's platform list in `creator-context`, using the stored format classification
- **What must survive the transformation**: ask the user if there's a specific line, argument, or detail that has to make it into the new version, don't assume every element of the original carries equal weight, let the user flag what actually matters most before cutting or expanding

## Compressing (long-form to short-form)

This is not summarizing. A summary describes what the piece said. A good compression keeps the sharpest single idea and makes it stand on its own, the way it would if it had been written short from the start.

- Identify the one core insight the long-form piece was actually built around, not just its opening line or its title
- Rebuild the piece in short-form format (hook, short paragraphs, closing question) around that core insight, per the format specs in `social-copywriting`
- Don't try to cram in every point the original made, a compression that references five different sub-arguments in 150 words reads as rushed, not efficient. Cutting is the actual work here, not condensing every sentence proportionally.
- Flag anything significant that got cut, so the user can confirm that's acceptable or tell you to preserve it a different way

## Expanding (short-form to long-form)

This is not padding. Adding filler sentences to hit a word count produces something that reads exactly like what it is. Real expansion adds genuine development the short version didn't have room for.

- Identify what the short-form piece implied but didn't have space to unpack, the reasoning behind the claim, an example, a counterpoint, a next-level implication
- Build the long-form structure (arc: problem, why it happens, the shift in thinking, what to do about it) around that core idea, per the format specs in `social-copywriting`
- Ask the user if they have specific material to add (an example, a story, data), since genuine expansion often needs input the short version never contained, rather than inventing detail to fill space
- If the user has nothing more to add and the idea genuinely doesn't support real long-form development, say so rather than padding it artificially, some ideas are correctly short and forcing them long produces weaker content, not more valuable content

## House style and voice

Apply the confirmed house style throughout, same as any other generated content. If the original draft already violates the house style (banned words, wrong punctuation), fix that as part of the transformation rather than carrying the violation into the new version, unless the user specifically wants the original wording preserved verbatim in parts.

## Presenting the result

Present the repurposed piece as plain text, ready to copy and paste, labeled with the direction and target format. If anything meaningful was cut or added, say so briefly before the piece itself, so the user can see the transformation's shape before reading the full text. Offer a `voice-qa` pass if the user wants extra confidence before publishing, especially useful here since a transformed piece can accidentally drift from house style even when the original didn't.
