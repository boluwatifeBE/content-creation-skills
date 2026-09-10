---
name: creator-context
description: Foundation skill for a full content creation system (calendar, copywriting, asset mining, repurposing, analysis, and more, across text and eventually video formats). Establishes format scope, then a default house style (voice, punctuation, banlist, formatting model, philosophy shape) the user can confirm or override, then captures the user's own persona (one or more fields, expertise, angle) and generates a tailored content philosophy from it, field-agnostic by design, works for any profession, and supports multi-discipline creators. Use this FIRST at the start of any content creation conversation, or whenever the user wants to reset/redefine their context within the same chat (e.g. "start over," "reset my context," "change my persona"). Every other skill in this system, both core skills and field-specific add-on packs, reads the persona, style, and profile established here.
---

# Creator Context: Foundation for Content Creation

This is the foundation skill for a full content creation system. It has three layers that must not be confused with each other:

1. **Format scope**: which kinds of content the user actually creates (text, video, or both), captured once so downstream skills know which rule sets apply.
2. **House style, as a default the user can override**: voice, punctuation, banlist, formatting model, and philosophy shape. These ship with sensible defaults, but none of them are forced on every user. Present them, let the user confirm or change them.
3. **The user's own persona and profile**: entirely dynamic, captured fresh from the user, never assumed to be any particular field.

Run this at the start of a new content conversation, or when the user explicitly wants to reset. Don't re-run it just because a new topic comes up within an already-established context.

## Step 1: Format scope

Ask which kinds of content the user actually creates: written content (captions, articles, posts), video content (scripts, scenes, moodboards), or both. Store this. It determines which rule sets in Step 2 apply, and which downstream skills are relevant, text-based skills for written formats, video-related packs (once built) for video. If the user only does one, don't burden them with rules for the other.

The rest of this skill currently defines the written-content rule set in full. A separate rule set for video (pacing, visual tone, scene language) is a future addition, not yet built, if the user selects video or both, note that video-specific rules are still being developed and proceed with whatever written-content elements still apply (persona, philosophy, and profile are format-agnostic and apply either way).

## Step 2: House style, default with override

Present the following as the **default house style**, then explicitly ask the user to confirm it as-is or tell you what to change. Don't apply any of this silently without that confirmation, and don't skip re-confirming it just because it's "the default," a default that's never actually been agreed to isn't a default, it's an assumption.

**Default tone**: natural and conversational, like a seasoned expert talking to a peer, not a marketing department. Vary sentence length for organic rhythm. Speak to real friction points and emotions, not just facts. Zero pretentiousness, direct, observant, quietly confident, never sounds like a textbook.

**Default punctuation rule**: never use em dashes or en dashes (— or –). Use commas, colons, semicolons, or a new sentence instead.

**Default banned words and phrases**: delve, elevate, synergy, revolutionize, testament, tapestry, landscape, paradigm, paradigm shift, game-changing, unlock, foster, dynamic, beacon, "in conclusion," "furthermore." The user can add to, remove from, or replace this list entirely.

**Default formatting model**: punchy hook-driven opening naming a real problem, no throat-clearing. Paragraphs 1 to 3 sentences, mobile-scannable. Bullets only for genuinely sequential/tactical steps. Close with an introspective question, never a generic "let me know in the comments."

**Formatting model, per-piece flexibility (system-wide principle, not a one-time setting)**: this default is a starting shape, not a rule every individual piece must obey. Every downstream skill that produces content inherits standing permission to propose deviating from it when a specific piece calls for something else, a reflective long-form essay that doesn't want a closing question, a technical breakdown that doesn't want a punchy hook. The permission is to *propose* the deviation and say why, not to silently apply it without mention or to rigidly force the default where it clearly doesn't fit. This applies system-wide so no individual skill has to decide on its own whether it's allowed to flex, it already is, consistently.

Once confirmed (as default or as edited by the user), apply this house style to all written content. Scan output against it before finalizing, if a banned word or an unconfirmed deviation slipped in, rewrite the sentence.

## Step 3: Capture the user's persona

Ask the user to describe themselves as a content creator. Most people won't know how much detail is useful, so guide them with a short prompt covering:

- **Field(s) or industry** (e.g. backend engineering, fashion design, brand strategy, fitness coaching, law, agriculture, anything). Make clear upfront that they can list more than one field if that's genuinely how they work, this system supports multi-discipline creators, don't make them awkwardly pick just one if it doesn't fit.
- **Specific specialization or niche** within each field
- **Experience or credibility markers**: years of experience, how they got here (formal training, self-taught, portfolio, client list), whatever is actually true for them
- **What sets them apart**: a distinctive skill, tool, opinion, or angle
- **Optional**: how they want to come across (mentor, contrarian, teacher, straight-shooter)

Offer a fill-in-the-blank format so they don't have to guess at structure, for example: *"I'm a [years] [role] who specializes in [niche]. I'm known for [distinctive angle]."* If they have multiple fields, they can list each briefly in the same format. They can answer loosely, this doesn't need to be formal.

### If more than one field is given: ask, don't assume

The moment the user lists two or more fields, ask one direct question before doing anything else, regardless of how related the fields seem: *"Do you want these under one account/identity with one shared voice and philosophy, or are these actually separate contexts (different audiences, maybe even different accounts) that should be set up separately?"*

Don't try to judge this yourself based on how related the fields sound. Fields that look closely related (like several design disciplines) and fields that look unrelated (like fitness coaching and 3D animation) get the exact same question, asked the same way, every time. The user knows their own audience better than any assumption Claude could make about which combinations "make sense" together. Let their answer decide it.

- If they want one shared identity: proceed through the rest of this skill once, with all fields captured together in Step 6.
- If they want separate contexts: help them finish this one first, then tell them clearly that for the other context, they should run `creator-context` again fresh (a new conversation, or an explicit reset within this one) rather than trying to hold two identities in one profile.

## Step 4: Generate and confirm the philosophy

From what the user gives you, write back two things:

1. A one-line **Identity statement**: who this content is written as.
2. A short **Core Philosophy** paragraph: what this person actually believes about their field that will come through in the content, a point of view, not a mission statement.

**Philosophy shape, default with override.** The default shape is a contrarian frame: "True [field] isn't about [surface-level thing], it's about [the deeper thing they actually believe]." This works well for a lot of fields and personas, but it isn't universal, some fields or personas fit a different shape more naturally. Offer it as the default, alongside two alternates the user can pick instead if the contrarian frame feels forced: a **straightforward declarative belief statement** (what they believe, stated plainly, no "not X" setup), or a **"what I've learned" framing** (an observation earned through experience, more reflective than declarative). Let the user choose a shape, or write their own if none fit.

Generate the philosophy from the specifics the user gave you, don't default to generic language, and don't pull from any other field's framing.

Present this back explicitly as a draft and ask the user to confirm or edit it before moving forward. Do not proceed to Step 5 until they've confirmed. This step matters because everything downstream is written in this identity, getting it wrong here means every future post is slightly off.

## Step 5: Brand & Business Profile

This profile is always about the person creating the content, the account these posts publish from, never a client, employer, or subject the user happens to be writing about. If the user does work for or about other people or brands (a designer discussing client work, a consultant analyzing other companies), that's just subject matter for individual posts, not the identity established here. If there's any ambiguity, say so directly: "Just to confirm, I mean your own account, not whichever company or project you're writing about."

Capture:

- **Account name/business**, if different from their personal name
- **Target audience**: who follows or should follow this account, and their main friction point or interest
- **Primary platforms, open list with known defaults, three format tiers**: this system classifies platforms into three tiers, not two, since a platform's actual character limit changes what's realistically writable there. The built-in platforms and their known tiers:
  - **Short-form**: X (280 characters), Threads posts (500 characters) and topic tags (50 characters), Instagram/TikTok Story captions (120 characters)
  - **Platform-native long post**: Instagram/TikTok main post captions (2,200 characters), Facebook post/reel captions (5,000 characters), LinkedIn Standard Post (3,000 characters)
  - **True long-form article**: LinkedIn Article, Medium, Substack (no practical character limit)

  Note that LinkedIn spans two different tiers depending on which format the user means, a LinkedIn Standard Post (capped, platform-native long post tier) and a LinkedIn Article (uncapped, true long-form tier) are genuinely different formats on the same platform. If the user just says "LinkedIn" without specifying which, ask which they mean, or capture both if they use both.

  If the user names a platform outside this list, capture it, then ask two questions: roughly what character limit does it have (or does it have none), and are there any length or style norms specific to it worth noting. Use the stated limit to place it in the correct tier (roughly under 500 characters is short-form, roughly 500 to 5,000 is platform-native long post, no practical limit is true long-form article, but let the user's actual answer decide rather than forcing it into a bucket that doesn't fit). Store the platform's name, its tier, and its specific character limit so downstream skills can check drafts against it directly, rather than needing a hardcoded rule for every platform that exists.
- **Content goals**: present this menu in plain language and let them pick more than one, most people are chasing several at once:
  - **Authority** — be seen as someone who knows this field deeply
  - **Education** — teach followers something they didn't know
  - **Community** — build a following that engages with each other, not just with you
  - **Leads/sales** — turn followers into clients or customers
  - **Promotional** — announce launches, offers, work, availability
  - **Personal brand/visibility** — just be known, independent of a specific business outcome
  - **Network/relationships** — get noticed by peers, collaborators, employers, or partners
  - **Documentation/portfolio** — build a public record of work over time, less about performance, more about having a trail

Restate the full profile back as a short summary so the user can correct anything before it's used downstream.

## Step 6: Store the field(s) for cross-skill matching

The field(s) captured in Step 3 are the reference list that field-specific add-on packs (e.g. `brand-identity-*`, `ux-research-*`, `animation-*`, `fitness-*`) check against before running. Every discipline has its own explicit pack in this system, there is no bundled multi-discipline pack, so a multi-field user like a brand identity designer who also works in UX research and brand strategy will install multiple packs, one per field, all reading from this same single context.

Keep the full field list clearly available for the rest of the conversation. The match check any pack performs is **list membership, not exact single match**: does the pack's declared field appear anywhere in the user's stated field list? If yes, proceed silently. If no, that pack is responsible for surfacing a soft warning (not a hard block) naming the mismatch and asking whether the user wants to proceed anyway. This skill's job is just to make sure the full field list is clearly established so that check is possible.

## Working principle: propose, don't assert

Across every skill in this system, treat interpretive claims (what a design choice means, what angle a topic should take, what a detail in an uploaded asset represents, whether a piece should deviate from the default format) as hypotheses or proposals to check with the user, not facts or decisions to present unilaterally. Bringing a strong, specific point of view is expected and good. Stating an invented meaning, or silently making a formatting or stylistic choice, as if it were confirmed when it hasn't been checked with the user, is not. When in doubt, propose and ask.

## Handoff to other skills

This context (format scope, house style, persona, philosophy, profile) is read by every other skill in this system: `content-calendar`, `social-copywriting`, `voice-qa`, `content-repurposing`, `hashtag-and-keyword`, `analyse-content`, `bio-and-profile-optimization`, `trend-to-content`, `engagement-reply-drafting`, `content-performance-review`, and any field-specific add-on pack. Don't restate the full house style or persona to the user each time another skill runs, just apply it silently, except where the per-piece flexibility principle calls for flagging a proposed deviation.
