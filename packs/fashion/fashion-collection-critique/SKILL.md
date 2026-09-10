---
name: fashion-collection-critique
description: Critiques a public collection, runway show, or brand's seasonal line using real fashion design frameworks, silhouette, construction, thematic cohesion, wearability versus spectacle, commercial viability, rather than a surface reaction to whether it's "nice." Use whenever the user wants to analyze, critique, or write about a public collection, a runway show, a competitor brand's line, or asks "what do you think of this collection/show." Requires creator-context to be active. This is a field-specific pack skill for Fashion, if the user's stated persona doesn't include fashion design or a clear equivalent, flag a soft warning before proceeding. Distinct from fashion-asset-to-content (which works from an asset the user already has from their own work) since the subject here is a public collection analyzed from what's observable and searchable.
---

# Fashion Collection Critique

Field pack skill for **Fashion**. Critiques a public collection, runway show, or brand's seasonal line using real design frameworks. The subject is a real designer or brand's public work, so accuracy and fairness matter as much here as in the other packs' teardown skills, and this field carries two specific extra risks: asserting a designer's intent behind a choice without any confirmation, and asserting commercial performance (sales, reception) that was never actually reported.

## Field match check (required first step)

Check whether the user's stated field(s) in `creator-context` include fashion design, fashion blogging, styling, or a clear equivalent. If not, surface a soft warning and ask whether to proceed anyway.

## Getting the subject

Ask whether the user has a specific collection, show, or brand line in mind, or wants one found.

- **If they have one**: use search to verify current, accurate details, when it showed or launched, what the actual pieces and concept were, and whether any credible source has reported on its reception or performance. Critiquing based on stale or wrong information undermines the whole piece.
- **If they want one found**: search for a recent or currently discussed collection or show relevant to the user's niche, bring back a small number of real candidates and let the user choose.

## Separating fact from read (critical distinction for this skill)

- **Confirmed facts**: what's actually visible in the collection, the silhouettes, fabrics, construction choices, styling, and anything the designer or brand has actually and verifiably stated about their own concept or intent (a show note, an interview, a published designer statement)
- **Interpretive read**: any claim about *why* a specific choice was made if it isn't confirmed by the designer, and any claim about commercial performance, sales, or critical reception unless a credible source actually reported it

**Never assert that a collection "sold well," "was a hit," or "flopped" without a real, cited source for that claim.** Sales and reception data for most collections is not public. If no such data is available, which is the normal case, frame the critique around craft and creative reasoning, not assumed outcomes.

**Never assign specific inspiration or meaning to a design choice unless the designer has actually stated it.** A guess at "what this color represents" or "why this silhouette was chosen" dressed up as insight is the same mistake as assigning meaning to an uploaded asset without confirmation, just applied to someone else's public work instead. Frame any such read explicitly as speculation: "this could read as..." not "this represents..."

## Analysis, using real frameworks

Once the subject and known facts are established, analyze using actual design frameworks relevant to what's observable:

- **Silhouette and construction**: technical execution, how the shapes are achieved, whether construction choices serve or fight the concept
- **Thematic cohesion**: does the collection hold together as a single idea, or read as disconnected pieces grouped by season alone
- **Wearability versus spectacle**: runway pieces often intentionally push beyond what's wearable, evaluate whether that reads as purposeful (a runway statement translating down to a wearable line) or just impractical without clear intent
- **Textile and material choices**: how fabric selection serves or undercuts the concept
- **Commercial and brand fit**: whether the collection makes sense relative to the brand's positioning and history, without asserting actual sales data

Choose whichever of these actually apply to the visible material, don't force all of them onto every critique.

## Fairness and tone

Critique the design choices, not the designer personally. Avoid personal attacks on named individuals. A critique can be genuinely critical, but it should be substantive, grounded in the frameworks above and actually visible evidence, not a dismissive reaction dressed up as analysis. Don't fabricate quotes and attribute them to real people, and follow standard copyright limits on anything actually quoted from a source.

## Generating the content

Produce one **short-form draft** and one **long-form draft**, per the user's platform format classifications in `creator-context`, following the confirmed house style. Keep the fact/read distinction visible in the copy itself, a reader should be able to tell what's confirmed versus the user's own interpretive read.

## Visual note

This skill cannot reproduce the collection's actual copyrighted imagery directly. Suggest the user attach their own photo or a properly credited press image when they post, rather than generating or recreating the designer's visual work.

## Carousel option

A point-by-point critique often works well as a carousel, each framework point or fact-vs-read observation becoming its own slide. Ask the user if they'd rather present this critique as a carousel instead of (or alongside) the two-draft output, and if so, hand off to `social-copywriting`'s carousel structure rather than building slides here.

## Presenting the output

Lead with a one or two sentence summary of the subject and the core angle, followed by both drafts, clearly labeled. If the user wants a more one-sided piece (all-critical or all-complimentary) rather than a balanced critique, that's their call, ask if unclear which they want.
