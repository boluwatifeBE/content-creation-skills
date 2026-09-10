---
name: content-repurposing
description: Transforms an existing piece of content, the user's own draft, a past post, or something social-copywriting produced earlier, from one format to another, between short-form, platform-native long post, and true long-form article tiers (scaling the rewrite's depth to the distance between tiers), or into/out of a platform-independent carousel (restructuring into or out of slides). Use whenever the user asks to "repurpose," "turn this into a," "shorten this for," "expand this into," "make a carousel out of this," "turn these slides into a post," or wants one piece of content adapted for a different platform or format than it was originally written for. Requires creator-context to be active for house style and platform character limits. Distinct from social-copywriting (which writes new copy from a topic) and asset-to-content (which mines a non-text asset like an image or PDF for a topic).
---

# Content Repurposing

Takes a piece of content that already exists and reshapes it for a different platform tier. The source material is always something the user already has, this skill never invents new subject matter, it transforms what's already there. The system this skill works within has **three tiers**, not two, so a transformation might be a small adjustment (moving within a tier, or one tier apart) or a genuinely large one (three tiers apart, an X post into a full Medium article), and the depth of rework needs to match the actual distance, not be treated as a single generic "make it shorter/longer" operation every time.

## Before starting

Confirm `creator-context` is active for house style and platform character limits. If not established, capture the essentials first.

Get the source content directly, pasted text, an uploaded file, or a reference to something already produced earlier in this conversation (e.g. "the LinkedIn post you wrote for me on Monday"). Don't work from a description of the content, get the actual text.

## Establishing the transformation

Confirm, if not already clear:

- **Source tier**: identify which tier the original content was written for, short-form, platform-native long post, true long-form article, or a carousel, based on its length, structure, and the platform it came from
- **Target platform or format**: pulled from the user's platform list in `creator-context`, using its stored tier and specific character limit, or **carousel**, if the user wants the content broken into slides instead. If the target is LinkedIn, confirm whether the user means the Standard Post (platform-native long post tier, 3,000-character cap) or the Article (true long-form tier, uncapped), these require genuinely different treatment
- **Distance between tiers**: same tier (a resize, e.g. Facebook post to LinkedIn Standard Post), one tier apart (a moderate compress or expand), or two tiers apart (a large compress or expand, e.g. a Medium article down to an X post, or an X post up to a full article). This distance determines how much real rework is needed, see below.
- **What must survive the transformation**: ask the user if there's a specific line, argument, or detail that has to make it into the new version, don't assume every element of the original carries equal weight, let the user flag what actually matters most before cutting or expanding

## Same-tier resize (minor)

Moving between two platforms in the same tier (Facebook to LinkedIn Standard Post, or X to a Threads post) is mostly a matter of fitting the specific character limit and adjusting tone slightly for the platform's norms, not a real content transformation. Trim or lightly pad as needed, but the core structure and depth stay the same. Check the result against the target platform's specific limit before presenting.

## Compressing (moving toward a shorter tier)

This is not summarizing. A summary describes what the piece said. A good compression keeps the sharpest single idea and makes it stand on its own, the way it would if it had been written short from the start.

- Identify the one core insight the source was actually built around, not just its opening line or its title
- Rebuild the piece at the target tier's format (per `social-copywriting`'s tier-specific specs) around that core insight, fit to the target platform's actual character limit
- **Scale the cut to the distance**: a one-tier compression (article down to a platform-native long post) can usually keep a supporting point or two alongside the core insight. A two-tier compression (article down to short-form) almost never can, at that distance, cutting down to the single sharpest point is the only way the piece survives the length, don't try to preserve secondary arguments that won't fit
- Don't try to cram in every point the original made, a compression that references five different sub-arguments in a 280-character post reads as rushed, not efficient. Cutting is the actual work here, not condensing every sentence proportionally.
- Flag anything significant that got cut, so the user can confirm that's acceptable or tell you to preserve it a different way (perhaps as a separate piece rather than jammed into this one)

## Expanding (moving toward a longer tier)

This is not padding. Adding filler sentences to hit a length produces something that reads exactly like what it is. Real expansion adds genuine development the shorter version didn't have room for.

- Identify what the source implied but didn't have space to unpack, the reasoning behind the claim, an example, a counterpoint, a next-level implication
- **Scale the development to the distance**: a one-tier expansion (short-form up to a platform-native long post) needs one or two genuine additions, an example, a bit more reasoning. A two-tier expansion (short-form up to a full article) needs a real arc: the problem, why it's actually happening, what the shift in thinking looks like, what to do about it, per `social-copywriting`'s true long-form tier specs, not just a longer version of the same three sentences
- Ask the user if they have specific material to add (an example, a story, data), since genuine expansion often needs input the shorter version never contained, rather than inventing detail to fill space. This matters more the further the expansion goes, a two-tier jump to a full article without any new material to work with is a real warning sign
- If the user has nothing more to add and the idea genuinely doesn't support the target tier's development, say so rather than padding it artificially. If a two-tier expansion isn't supported, suggest the one-tier version instead as a more honest target, some ideas are correctly short, and forcing them into a full article produces weaker content, not more valuable content

## Transforming into a carousel

Breaking existing content into a carousel isn't a compression or expansion in the tier-distance sense, it's a restructuring: the same underlying ideas get redistributed across discrete slides rather than shortened or lengthened as continuous prose.

- Identify the distinct points the source content makes, a long-form article typically already has natural section breaks that map to slides, a single short-form post usually has one core idea that needs to be broken open into its component parts to fill multiple slides credibly
- If the source doesn't actually contain enough distinct points to fill a reasonable slide count, say so rather than manufacturing thin slides just to hit a number, ask whether the user wants a shorter carousel or has more material to add
- Build the result following `social-copywriting`'s carousel structure: title/hook slide, framing slide, body slides (one point per slide), closing engagement slide, each with its own visual direction note
- Don't lose the source's core argument or reorder it in a way that changes its logic, restructuring into slides should preserve what the piece actually says, not just chop it into arbitrary chunks

## Transforming a carousel into a standard post

Consolidating carousel slides back into a single continuous piece (short-form, platform-native long post, or true long-form article) means finding the throughline that connects the slides and writing it as continuous prose, not just concatenating the slide text.

- Identify the core argument the carousel built slide by slide, and rebuild it as flowing prose at the target tier, following the same compress/expand distance logic above if the target tier is shorter or longer than the carousel's total content would naturally support as prose
- The visual direction notes don't carry over, they were instructions for slide design, not content, drop them from the consolidated version

## House style and voice

Apply the confirmed house style throughout, same as any other generated content. If the original draft already violates the house style (banned words, wrong punctuation) or doesn't fit the target platform's character limit, fix that as part of the transformation rather than carrying the violation into the new version, unless the user specifically wants the original wording preserved verbatim in parts.

## Length check before presenting

Before presenting a transformed piece targeting a platform tier, check its actual character count against the target platform's specific limit (per `social-copywriting`'s platform table). Don't present something that doesn't fit without flagging it. This check doesn't apply when the target is a carousel, since carousels aren't bound to a platform character limit, check instead that the slide count and per-slide text length are reasonable per `social-copywriting`'s carousel structure.

## Presenting the result

Present the repurposed piece as plain text, ready to copy and paste, labeled with the source tier, target platform, and distance (e.g. "compressed two tiers: Medium article → X post"). If anything meaningful was cut or added, say so briefly before the piece itself, so the user can see the transformation's shape before reading the full text. Offer a `voice-qa` pass if the user wants extra confidence before publishing, especially useful here since a transformed piece can accidentally drift from house style, or exceed the target's character limit, even when the original didn't.
