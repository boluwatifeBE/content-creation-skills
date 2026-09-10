---
name: branding-teardown
description: Critiques a public brand's identity, rebrand, or strategic positioning (a competitor, a recent rebrand, a well-known company) using real brand strategy frameworks, positioning, differentiation, brand architecture, rather than a surface reaction to how a logo looks. Use whenever the user wants to analyze, critique, or write about a public brand or rebrand, asks "what do you think of this rebrand," or wants a teardown-style post about a company that isn't their own client work. Requires creator-context to be active. This is a field-specific pack skill for Brand Identity Design and Brand Strategy, if the user's stated persona doesn't include either, flag a soft warning before proceeding. Distinct from branding-asset-to-content (which works from an uploaded asset the user has) since the subject here is a public brand analyzed from what's observable and searchable.
---

# Branding Teardown

Field pack skill for **Brand Identity Design and Brand Strategy**. Critiques a public brand, a rebrand, a competitor, a well-known identity system, using real strategic frameworks rather than a surface-level reaction. This is one of the most common content formats in this field ("why the new [brand]'s rebrand works, or doesn't"), and it carries a different kind of risk than any other skill in this pack: the subject is a real company, not the user's own or client work, so accuracy and fairness matter more here than anywhere else in the system.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include brand identity design, brand strategy, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Getting the subject

Ask whether the user has a specific brand or rebrand in mind, or wants one found.

- **If they have one**: use search to verify current, accurate details before critiquing anything, when the rebrand happened, what actually changed, and whether the company published its own stated rationale. Critiquing a rebrand based on stale or wrong information undermines the whole piece.
- **If they want one found**: search for a recent or currently discussed rebrand or brand move relevant to the user's niche, bring back a small number of real candidates and let the user choose rather than assuming which one they'd want to write about.

## Separating fact from read (critical distinction for this skill)

This is the most important discipline in this skill, more than anywhere else in the system, because the subject is a real company Claude has no inside knowledge of.

- **Confirmed facts**: what visibly changed (the mark, the color, the typography, the tone), and anything the company has actually and verifiably stated about its own rationale (a press release, an interview, an official case study from the design agency involved)
- **Interpretive read**: any claim about *why* the company made a choice, what problem it was really solving, whether it will work, that isn't directly confirmed by something the company said

Never present an interpretive read as if it were a confirmed fact. Always frame it explicitly as a read: "my take on why this works" or "what this seems to be solving for," not "this is why they did it." This is the same discipline as the propose-don't-assert principle elsewhere in this system, applied here to real companies who never confirmed anything to the user directly.

## Analysis, using real frameworks

Once the subject and known facts are established, analyze using actual strategic frameworks relevant to what's observable:

- **Positioning and differentiation**: does the identity clarify or blur what makes this brand different from its competitors
- **Brand architecture**: if relevant, how this fits with any parent brand or sub-brand structure
- **Consistency and scalability**: does the system hold up across the applications visible (packaging, digital, signage), or does it show strain
- **Tone of voice alignment**: does the verbal identity (if visible in the same materials) match the visual shift, or do they pull in different directions
- **Market and competitive context**: does this make sense relative to what competitors in the same category are doing, a choice that looks strange in isolation may make complete sense as differentiation from a crowded field

Choose whichever of these actually apply to the visible material, don't force all of them onto every teardown.

## Fairness and tone

Critique the strategic and design choices, not the people who made them. Avoid personal attacks on named individuals (a CEO, a specific in-house designer), the subject is the work and the thinking behind it, not anyone's competence or character. Don't fabricate quotes and attribute them to real people, if quoting someone, only use something they're actually verified to have said, found through search, and follow standard copyright limits on how much of any single source can be quoted directly.

A teardown can be genuinely critical, this isn't about being uniformly positive, but it should be substantive criticism grounded in the frameworks above, not a dismissive reaction ("this is ugly") dressed up as analysis.

## Generating the content

Produce one **short-form draft** and one **long-form draft**, per the user's platform format classifications in `creator-context`, following the confirmed house style. Keep the fact/read distinction visible in the copy itself where it matters, a reader should be able to tell what's verified versus the user's own strategic read.

## Visual note

This skill cannot reproduce the brand's actual logo or copyrighted visual material directly. Suggest the user attach official rebrand imagery themselves (a screenshot, a press image) when they post, rather than generating or recreating the brand's visual assets.

## Carousel option

A point-by-point critique often works well as a carousel, each framework point or fact-vs-read observation becoming its own slide. Ask the user if they'd rather present this critique as a carousel instead of (or alongside) the two-draft output, and if so, hand off to `social-copywriting`'s carousel structure rather than building slides here.

## Presenting the output

Lead with a one or two sentence summary of the subject and the core angle, followed by both drafts, clearly labeled. If the user wants a more one-sided piece (all-critical or all-complimentary) rather than a balanced teardown, that's their call to make, ask if unclear which they want, since this affects tone throughout.
