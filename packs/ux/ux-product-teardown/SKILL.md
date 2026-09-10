---
name: ux-product-teardown
description: Critiques a public product's user experience, an app's onboarding, a checkout flow, a navigation pattern, using real UX frameworks like usability heuristics, cognitive load, and accessibility, rather than a surface reaction to how something looks. Use whenever the user wants to analyze, critique, or write about a public product's UX, a competitor's flow, or a well-known app's design decisions, or asks "what do you think of this onboarding/checkout/flow." Requires creator-context to be active. This is a field-specific pack skill for UX/Product Research and Design, if the user's stated persona doesn't include either, flag a soft warning before proceeding. Distinct from ux-asset-to-content (which works from an asset the user already has from their own work) since the subject here is a public product's live experience.
---

# UX Product Teardown

Field pack skill for **UX/Product Research and Design**. Critiques a public product's user experience using real usability and research frameworks. This carries a different kind of risk than the branding version of this skill: a rebrand is a discrete, announced event that can be verified through search, but a product's UI changes constantly and often silently, so accuracy here depends on seeing the actual current flow, not recalling what an app used to look like.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include UX, product research, product design, UX engineering, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Getting the subject: accuracy requires current, direct evidence

Ask the user for actual screenshots, a screen recording description, or a precise, current walkthrough of the flow being critiqued, rather than relying on a general memory of what the product looks like. Apps and websites redesign frequently, sometimes just for a subset of users through A/B testing, so a critique based on stale or assumed knowledge of the interface risks being flatly wrong about what's actually there right now.

If the user doesn't have screenshots and wants to discuss the product from general knowledge, say plainly that the critique may not reflect the current live version, and recommend they verify or capture the current flow before publishing anything based on it.

## Separating fact from read (critical distinction for this skill)

This is the most important discipline in this skill, arguably even more than the branding teardown version, because there is no equivalent to a company's "published rationale" for most UX decisions, teams rarely explain why a specific flow works the way it does.

- **Confirmed facts**: what's actually visible in the screenshots or described flow, the steps, the copy, the visual hierarchy, the number of taps or fields
- **Interpretive read**: any claim about *why* the team designed it this way, what usability testing supposedly showed, or how users actually respond to it

Never assert a claim about real user behavior or testing data that hasn't been confirmed, phrases like "users clearly struggle with this" or "this is why conversion drops here" are fabricated data dressed as fact unless the user has actually provided real analytics or testing results. Frame every behavioral claim explicitly as a read: "this step looks like it could introduce friction because..." not "this step causes users to drop off."

## Analysis, using real frameworks

Once the subject and known facts are established, analyze using actual UX frameworks relevant to what's observable:

- **Usability heuristics**: visibility of system status, consistency, error prevention, recognition over recall, and similar established principles, applied to what's actually visible
- **Cognitive load**: how much the user has to hold in mind or figure out at each step
- **Information architecture**: whether the flow's structure matches how a user would naturally think about the task
- **Accessibility**: visible issues like contrast, tap target size, or reliance on color alone to convey information, only where genuinely observable, not assumed
- **Friction relative to the task's stakes**: a small amount of friction may be entirely appropriate for a high-stakes action (payment, account deletion) and a real problem for a low-stakes one (browsing)

Choose whichever of these actually apply to the visible material, don't force all of them onto every teardown.

## Fairness and tone

Critique the design choices, not the people or team who made them. Avoid personal attacks on named individuals. A teardown can be genuinely critical, but it should be substantive criticism grounded in the frameworks above and the actual visible evidence, not a dismissive reaction dressed up as analysis.

## Generating the content

Produce one **short-form draft** and one **long-form draft**, per the user's platform format classifications in `creator-context`, following the confirmed house style. Keep the fact/read distinction visible in the copy itself where it matters, a reader should be able to tell what's directly observable versus the user's own interpretive read.

## Visual note

Recommend the user include their own screenshot or recording of the actual flow being discussed, since the whole credibility of a UX teardown rests on the reader being able to see exactly what's being critiqued.

## Carousel option

A point-by-point critique often works well as a carousel, each framework point or fact-vs-read observation becoming its own slide. Ask the user if they'd rather present this critique as a carousel instead of (or alongside) the two-draft output, and if so, hand off to `social-copywriting`'s carousel structure rather than building slides here.

## Presenting the output

Lead with a one or two sentence summary of the subject and the core angle, followed by both drafts, clearly labeled. If the user wants a more one-sided piece (all-critical or all-complimentary) rather than a balanced teardown, that's their call, ask if unclear which they want.
