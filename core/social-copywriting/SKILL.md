---
name: social-copywriting
description: Writes actual, publish-ready social media copy the user can copy and paste directly onto whichever platforms their creator-context profile defines, short-form (Instagram, X, or custom platforms classified as short-form) or long-form (LinkedIn, Medium, Substack, or custom platforms classified as long-form). Use whenever the user asks to write a caption, post, article, hook, or copy, wants to turn a topic or a content-calendar entry into a finished piece, or asks to "draft," "write," or "flesh out" a specific post. Requires creator-context to be active first for persona, house style, and philosophy; if not active, establish it briefly before writing. Distinct from content-calendar (which plans what to post and when) and asset-to-content (which mines an uploaded file for the topic).
---

# Social Copywriting

Produces the actual, finished, copy-and-paste-ready text for a specific piece of content. Where `content-calendar` plans what to post and when, and `asset-to-content` extracts what to write about from an uploaded file, this skill is where a topic becomes finished copy in the user's confirmed voice.

## Before writing

Confirm `creator-context` is active (persona, house style, philosophy, and profile). If it isn't established yet, capture the essentials first rather than writing in a generic voice.

### Draft-or-generate checkpoint (ask before writing)

Never assume the user is starting from a blank page. Ask: *"Do you already have a rough draft, some notes, or a specific opinion you want shaped into a post, or should I write this from scratch?"*

- If they have something started: work from their actual words and structure. Sharpen it, fit it to the house style and format, and fix anything that violates a hard constraint (banned words, dashes), rather than replacing their voice with a generic one.
- If they want it from scratch: proceed with the rest of this skill.
- Either way, present the result as an editable draft, invite changes rather than treating it as final.

## Establishing the piece

Confirm, if not already clear from the request:

- **The topic or angle**: what is this post actually about, and what's the one real insight or lesson it delivers? A post without a specific point isn't ready to write. If the topic is vague, ask one clarifying question or propose a sharp angle and confirm before drafting, don't invent a take and present it as decided.
- **The platform(s)**: pull from the user's actual platform list in `creator-context`. Platforms sharing a format classification (short-form or long-form) are treated as interchangeable, write one draft per format type unless the user wants platform-specific variants (e.g. "make the X version punchier and shorter than the Instagram one").

## Format specs by classification

**Short-form (Instagram, X, or any custom platform classified as short-form)**
- Hook line first: names the real problem or tension in one line, no throat-clearing
- Body: 3 to 8 short paragraphs (1 to 3 sentences each), builds the insight, doesn't just describe it
- Closes with an introspective question by default, per the house style's formatting model, unless a deviation has been proposed and agreed (see below)
- Length: tight enough to read in one scroll, roughly 80 to 200 words unless the user asks for shorter or longer

**Long-form (LinkedIn, Medium, Substack, or any custom platform classified as long-form)**
- Same hook-first opening, but room to develop the idea with a real arc: the problem, why it's actually happening, what the shift in thinking looks like, what to do about it
- Subheadings only if the piece is long enough to need them (roughly 600+ words), don't force structure onto a shorter piece
- Bullets only for genuinely sequential or tactical content, not as an organizing crutch
- Closes the same way by default: an introspective question, not a generic CTA
- Length: no hard cap, let the idea determine length, but don't pad. If the user gave a word count, hit it.

## Per-piece formatting flexibility

The formatting model above is the house default, not a rigid requirement for every piece. If a specific piece would genuinely read better without part of it, a reflective essay that doesn't want a closing question, a technical breakdown that doesn't want a punchy hook, propose that deviation explicitly and say why, then proceed based on the user's answer. Don't silently deviate, and don't force the default where it clearly doesn't serve the piece.

## Voice enforcement

Every draft must be checked against the house style confirmed in `creator-context` before it's presented as finished: the confirmed tone, the confirmed punctuation rule, the confirmed banlist (default or user-modified), and the confirmed formatting model (or an agreed deviation). If a first draft violates any of these, rewrite the offending sentence rather than delivering it with a note, the user shouldn't have to edit out a banned word or a stray dash themselves.

## Working from a content-calendar entry

If the user references a calendar entry ("draft the Tuesday LinkedIn post" or similar), pull the pillar, hook, and angle already established for that slot rather than starting from scratch, expand it into the full format above.

## Presenting the draft

Present the finished copy as plain text, ready to copy and paste, not inside a code block. Label which platform(s) or format type it's written for. If the user wants to see how it would look on the platform itself, that's a visual concern, hand off to `visual-direction` if that skill is active, otherwise just note that a visual pairing is worth considering.

If the user wants revisions, edit the existing draft rather than regenerating from scratch, unless they ask for a completely different angle.
