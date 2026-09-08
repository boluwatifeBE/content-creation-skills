# Contributing to Content Creation Skills

Thanks for wanting to improve this. This system only stays useful if the skills in it stay disciplined, so this doc is less "here's how to open a PR" and more "here's what every skill in this repo has already had to learn the hard way." Read the [design principles in the README](README.md#design-principles-behind-every-skill) first, this file assumes you have.

---

## Table of contents

- [Ways to contribute](#ways-to-contribute)
- [Before you start](#before-you-start)
- [SKILL.md format requirements](#skillmd-format-requirements)
- [The core-vs-pack neutrality problem (a real case study)](#the-core-vs-pack-neutrality-problem-a-real-case-study)
- [Writing style for skill instructions](#writing-style-for-skill-instructions)
- [Validation checklist before you open a PR](#validation-checklist-before-you-open-a-pr)
- [Proposing a new skill](#proposing-a-new-skill)
- [Proposing a new field pack](#proposing-a-new-field-pack)
- [Changing a core skill (extra caution required)](#changing-a-core-skill-extra-caution-required)
- [Reporting a bug or unclear behavior](#reporting-a-bug-or-unclear-behavior)
- [PR process](#pr-process)
- [License](#license)

---

## Ways to contribute

- Fix or sharpen an existing skill's instructions
- Propose a new skill within an existing pack
- Propose an entirely new field pack
- Improve the README or this file
- Report a bug: a skill that doesn't ask what it should, invents something it shouldn't, or triggers when it shouldn't

All of these are welcome, and none require deep familiarity with every skill in the repo, just the specific one you're touching and the design principles that apply everywhere.

---

## Before you start

Check open issues and discussions first, someone may already be working on the same skill or pack. If you're proposing something new rather than fixing something broken, open an issue before writing the full `SKILL.md`, it's a much smaller conversation to have before the work exists than after.

---

## SKILL.md format requirements

Every skill is a folder containing one `SKILL.md`, following the [Agent Skills](https://agentskills.io) spec:

```
core/<skill-name>/SKILL.md
packs/<pack-name>/<skill-name>/SKILL.md
```

**Frontmatter requirements:**

```yaml
---
name: skill-name-here
description: A specific, third-person description of what this skill does and when it should trigger.
---
```

- `name` must exactly match the folder name, lowercase, hyphenated.
- `description` is what determines whether the skill actually gets used, be specific about trigger phrases and conditions, not vague ("helps with content" triggers unreliably; "use whenever the user asks to plan, schedule, or asks for a content calendar" triggers reliably).

**A real gotcha, learned the hard way**: a colon inside the `description` field can break YAML parsing entirely (`mapping values are not allowed here`), since YAML reads an unescaped colon as a new key-value pair even mid-sentence. Avoid colons in the description, use a comma or restructure the sentence instead. Always validate the frontmatter parses before submitting, see the checklist below.

---

## The core-vs-pack neutrality problem (a real case study)

This actually happened during this repo's development, and it's the single most useful thing to understand before writing a skill.

`asset-to-content` was originally built as one general-purpose **core** skill, meant to work for any field. It was built and tested almost entirely against a brand identity design use case. The instructions ended up with lines like *"name what kind of artifact this is: a logo grid, a conversion funnel spreadsheet, a UX wireframe, a brand mood board, a pitch deck slide"*, which reads as a helpful, concrete example list. It's also entirely design-and-branding-flavored. A backend engineer or a fashion designer using that "neutral" skill would have gotten measurably worse results, because the skill's own illustrative examples silently assumed a design context, even though nothing in the skill's stated purpose said it should.

The fix wasn't to make the examples vaguer, vague examples make a skill *less* useful. The fix was recognizing that a genuinely useful example list is inherently field-specific, and that's fine, as long as the skill is honest about being field-specific. `asset-to-content` was retired and split into `branding-asset-to-content`, `ux-asset-to-content`, and `marketing-asset-to-content`, each free to lean fully into its own field's real vocabulary, with the neutral core reserved for skills that genuinely don't need domain examples to function (`content-calendar`, `voice-qa`, and similar).

**The rule this produces for contributors:**

- **Writing or editing a core skill?** Any illustrative example you add should work for a random, unrelated field as a sanity check. If you catch yourself reaching for a design, marketing, or engineering-specific example to illustrate a core skill's instructions, that's the signal to either make the example genuinely generic or reconsider whether the skill is actually pack material.
- **Writing or editing a pack skill?** Lean into field-specific vocabulary and examples deliberately. A `branding-*` skill that avoids saying "logo grid" or "brand mood board" for fear of being too specific is failing at the entire point of a pack.

---

## Writing style for skill instructions

`SKILL.md` instructions are written **to Claude, about the user**, not to the end user directly. Keep this consistent:

- Use imperative/directive phrasing: "Ask the user whether...", "Confirm before proceeding...", "Never invent a metric that wasn't provided."
- Be concrete about what triggers what. "Ask if unclear" is weaker than "if the user hasn't specified X, ask directly: '...'"
- Every checkpoint (draft-or-generate, direction confirmation, field mismatch) should specify what happens on each answer, not just that a question gets asked.
- Avoid padding a skill to look thorough. A shorter skill that's actually followed precisely is better than a longer one restating the same instruction three ways.

---

## Validation checklist before you open a PR

- [ ] `name` in frontmatter exactly matches the folder name
- [ ] `description` has no unescaped colons or other characters that could break YAML (test this, don't just eyeball it)
- [ ] `description` is specific enough to trigger reliably, and states what the skill requires (usually `creator-context` being active)
- [ ] If this is a pack skill, it includes the field match check as its first real step
- [ ] If this skill produces content, it includes a draft-or-generate checkpoint rather than assuming a blank page
- [ ] If this skill could state a claim about a real, named third party, it enforces fact-vs-read separation
- [ ] If this skill touches money, performance, or outcomes, it explicitly forbids inventing a number
- [ ] If this skill touches tools, platforms, or products, it requires disclosure of any paid/affiliate relationship
- [ ] The skill doesn't duplicate an existing skill's stated purpose, if it's genuinely similar to something that exists, the PR description should explain why it's distinct
- [ ] You've actually run the skill in a live conversation with a test persona and confirmed it behaves as written, not just read the instructions back to yourself

---

## Proposing a new skill

Open an issue with:

- **What the skill would do**, specifically, not just a name
- **Why it needs to be its own skill** rather than an addition to an existing one, most requests are better served by improving an existing skill than adding a new one
- **Whether it's core or pack-specific**, and if pack-specific, which pack and why it wouldn't fit an existing skill in that pack

---

## Proposing a new field pack

This repo currently covers branding, UX/product research, and marketing. Programming, animation, fitness, culinary, and any other field are all reasonable candidates. Include in your proposal:

1. **Field name and scope**, be explicit about how broad or narrow (e.g. "Business Marketing" spans paid/email/SEO/content deliberately, a narrower pack might not)
2. **The two baseline skills**: `<field>-asset-to-content` and `<field>-content-ideation`, drafted for what a real asset and real topic ideation actually look like in that field
3. **Field-specific additions with rationale**. Don't copy another pack's skill list by default, think about what that field's actual content risks and patterns are. The UX and marketing packs both got a tool/platform-spotlight skill because those fields move fast and carry real disclosure risk, the branding pack didn't need one for the same reason a teardown skill needed extra fact/read discipline that a glossary skill didn't.
4. **A `<field>-confidential-story` skill**, if the field involves any client-facing or otherwise confidential work, most professional fields do

**On combining fields into one pack**: only do this when the fields are genuinely inseparable in real practice, the way Brand Identity Design and Brand Strategy are (you can't defend a visual choice without the positioning underneath it). Adjacent isn't the same as inseparable. When in doubt, keep packs separate, a multi-disciplinary user can always install more than one.

---

## Changing a core skill (extra caution required)

Every pack skill in this repo reads from the 11 core skills, `creator-context` especially. A change to a core skill's behavior potentially affects every pack, not just the one you're thinking about while making the change.

If your PR touches a core skill:
- State explicitly in the PR description which packs you checked for downstream impact
- If the change affects how `creator-context` stores or structures information (the field list, platform classifications, house style), check that every pack's field-match check and format-classification logic still works against the new structure
- Prefer additive changes (a new optional field, a new classification option) over changes that alter the shape of existing data other skills already depend on

---

## Reporting a bug or unclear behavior

Open an issue with:

- Which skill
- What you asked for (the actual prompt, or close to it)
- What happened
- What you expected to happen instead, and ideally, which design principle or instruction in the skill you'd expect to have prevented it

---

## PR process

1. Fork the repo, branch from `main`
2. Make your change, run through the validation checklist above
3. Open a PR describing what changed and why, link any related issue
4. Expect review against the design principles and checklist, not just "does it work," a skill that produces good output by accident but doesn't ask the right questions along the way still needs revision

---

## License

By contributing, you agree your contribution is licensed under the same MIT License as the rest of this repo.
