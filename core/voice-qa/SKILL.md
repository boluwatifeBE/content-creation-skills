---
name: voice-qa
description: Checks a piece of draft content against the house style confirmed in creator-context (banlist, punctuation rule, tone, formatting model) and flags specific violations with suggested fixes. Use whenever the user asks to review, check, proofread, or QA a piece of copy for voice or style compliance, asks "does this sound like me," or wants a draft checked before publishing. Works on drafts from any source, something social-copywriting produced earlier in the conversation, a piece the user pasted in, or an uploaded file. Requires creator-context to be active; if it isn't, ask what house style to check against before proceeding.
---

# Voice QA

A mechanical compliance check, not a rewrite from scratch. This skill exists to catch what slipped through, a banned word, a stray em dash, a paragraph that ran long, a formatting model violation that was never actually agreed to as a deviation, before the user publishes something that doesn't match their confirmed voice.

## Before checking

Confirm `creator-context`'s house style is active (banlist, punctuation rule, tone, formatting model, and any per-piece deviations the user already agreed to for this specific piece). If house style has never been established, ask what to check against rather than inventing a standard, this skill has no default opinions of its own, it only enforces what the user already confirmed elsewhere.

If the user says a specific deviation was already agreed for this piece (no closing question, no hook, whatever), take that at face value rather than flagging it as a violation, the point of per-piece flexibility is that an agreed deviation isn't an error.

## What to check

Go through the draft methodically against each confirmed element:

- **Banned words/phrases**: scan for every entry in the confirmed banlist (default or user-modified). Flag each occurrence.
- **Punctuation rule**: scan for em dashes or en dashes if that rule is active. Flag each occurrence.
- **Tone**: read for whether the piece actually sounds like the confirmed tone, conversational and direct by default, or whatever the user customized it to. This is more judgment-based than the mechanical checks above, flag places where it drifts into something stiffer, more corporate, or more generic than the confirmed voice, and say specifically what reads off, not just that something feels wrong.
- **Formatting model**: check hook presence, paragraph length, bullet usage, and closing question against the confirmed model, accounting for any agreed per-piece deviation. Flag any unagreed deviation as a violation, not as a stylistic choice.
- **Anything else the user has specifically asked this skill to watch for**, if they've mentioned a personal pet peeve or rule not captured elsewhere in `creator-context`, apply it here too.

## Presenting results

Don't just declare "pass" or "fail." For each issue found:

- Quote or point to the specific sentence or phrase
- Name which rule it violates
- Propose a specific fix, not just "rewrite this"

If the draft is clean, say so plainly rather than inventing minor nitpicks to seem thorough, a genuinely compliant draft doesn't need manufactured feedback.

## Fixing

Ask whether the user wants you to apply the fixes directly and return a corrected version, or whether they'd rather see the flagged list and make the edits themselves. Don't rewrite the whole piece unprompted, when fixing, touch only the flagged sentences, preserve everything else exactly as written, since a QA pass isn't an invitation to also improve unrelated parts of the draft.

## Scope

This skill checks house style compliance only. It doesn't evaluate whether the content's argument is any good, whether the topic is compelling, or whether the strategy behind the piece is sound, that's a different kind of feedback, and if the user wants that too, say so and ask if they want broader feedback beyond style compliance.
