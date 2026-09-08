# Content Creation Skills

A modular system of [Agent Skills](https://agentskills.io) for social media content creation, built for Claude. One shared foundation captures who you are and how you write, once. Everything else, planning, drafting, analysis, and field-specific specialist skills, reads from that foundation instead of guessing or repeating itself.

This is not a single "write my posts" skill. It's a small operating system for content creation: a **core** of field-agnostic tools that work for literally any profession, plus **field packs** that add real, framework-grounded depth for specific disciplines (branding, UX, marketing, and more to come).

---

## Table of contents

- [What this actually does](#what-this-actually-does)
- [Installing a skill](#installing-a-skill)
- [How the system is structured](#how-the-system-is-structured)
- [Defaults vs. what you control](#defaults-vs-what-you-control)
- [The core skills (11)](#the-core-skills-11)
- [Field packs](#field-packs)
  - [Branding (Brand Identity Design + Brand Strategy)](#branding-pack)
  - [UX / Product Research](#ux-pack)
  - [Business Marketing](#marketing-pack)
- [How to use this system](#how-to-use-this-system)
  - [Core skills alone](#core-skills-alone)
  - [Core + one field pack](#core--one-field-pack)
  - [A single field-pack skill directly](#a-single-field-pack-skill-directly)
  - [Combining two or more field packs](#combining-two-or-more-field-packs)
  - [What the mismatch warning means](#what-the-mismatch-warning-means)
- [Filling out your persona](#filling-out-your-persona)
- [Design principles behind every skill](#design-principles-behind-every-skill)
- [Repository structure](#repository-structure)
- [Contributing](#contributing)
  - [Updating an existing skill](#updating-an-existing-skill)
  - [Suggesting a new skill](#suggesting-a-new-skill)
  - [Proposing a new field pack](#proposing-a-new-field-pack)
  - [The one mistake to avoid](#the-one-mistake-to-avoid)
- [FAQ](#faq)
- [License](#license)

---

## What this actually does

Most "AI content" prompts either sound like nobody, or sound like whoever wrote the prompt. This system is built to sound like *you*: your field, your experience, your actual point of view, your platforms. It does that by separating two things that usually get tangled together:

1. **A foundation skill (`creator-context`)** that captures your voice, your persona, and your business profile once, and that every other skill reads from.
2. **Everything else**, which either works for any profession (the core skills) or adds real depth for a specific one (field packs).

Nothing in this system writes generic marketing-speak by default. Every skill is built to ask before assuming, propose before asserting, and admit when it doesn't have enough information, rather than confidently filling gaps with plausible-sounding invention.

---

## Installing a skill

Each skill in this repo is a folder containing one `SKILL.md` file, following the [Agent Skills](https://agentskills.io) format. How you install depends on where you're using Claude:

- **claude.ai**: go to **Customize → Skills**, click **+ → Create skill**, and upload a `.skill` file (or a zipped skill folder) for each skill you want. Skills you upload are private to your account by default.
- **Claude Code / other compatible agentic tools**: copy the relevant skill folder(s) into the tool's skills or agents directory, following that tool's own setup instructions.
- **Team/Enterprise workspaces**: an org owner can provision a skill account-wide under Organization settings, if you want your whole team using the same setup.

Install `creator-context` first. It's the only skill every other skill in this system depends on.

---

## How the system is structured

```
core/                       Field-agnostic. Works for any profession.
  creator-context/           <- start here, always
  content-calendar/
  social-copywriting/
  voice-qa/
  content-repurposing/
  hashtag-and-keyword/
  analyse-content/
  bio-and-profile-optimization/
  trend-to-content/
  engagement-reply-drafting/
  content-performance-review/

packs/
  branding/                  Brand Identity Design + Brand Strategy (combined)
    branding-asset-to-content/
    branding-content-ideation/
    branding-teardown/
    branding-case-study-builder/
    branding-glossary-explainer/
    branding-confidential-story/

  ux/                        UX / Product Research and Design
    ux-asset-to-content/
    ux-content-ideation/
    ux-product-teardown/
    ux-case-study-builder/
    ux-glossary-explainer/
    ux-tool-and-workflow-spotlight/
    ux-confidential-story/

  marketing/                 Business Marketing (paid, email, SEO, content, strategy)
    marketing-asset-to-content/
    marketing-content-ideation/
    marketing-campaign-teardown/
    marketing-case-study-builder/
    marketing-glossary-explainer/
    marketing-tool-and-platform-spotlight/
    marketing-confidential-story/

  <your-field>/               More packs welcome, see Contributing
```

**Core skills never assume a field.** They read whatever persona `creator-context` captured and work from that, whether it says "backend engineer" or "wedding photographer." **Field packs are explicit on purpose.** Every discipline gets its own named pack (`branding-*`, `ux-*`, `marketing-*`), nothing is bundled into a single "creative professional" or "business professional" catch-all, because that would silently assume every user in a broad category needs the same specialist skills. If you're multi-disciplinary, you install more than one pack, see [Combining two or more field packs](#combining-two-or-more-field-packs).

---

## Defaults vs. what you control

`creator-context` ships with sensible defaults so you're not stuck answering a long questionnaire before you can post anything. But nothing is force-fed. Every default is presented explicitly and can be confirmed or changed.

| Element | Status |
|---|---|
| Tone (natural, conversational, zero pretentiousness) | Default, confirm or override |
| Punctuation rule (no em/en dashes) | Default, confirm or override |
| Banned words/phrases list | Default, add to / remove from / replace entirely |
| Formatting model (hook, short paragraphs, closing question) | Default, override per-piece any time (see below) |
| Philosophy shape (contrarian frame / declarative / "what I've learned") | Default is the contrarian frame, two alternates offered, or write your own |
| Format scope (text, video, or both) | Always asked, never assumed |
| Persona, field(s), audience, platforms, goals | **Always yours.** Nothing built in, nothing assumed. |

**Per-piece formatting flexibility** deserves its own note: the formatting model is a house default, not a rule every individual piece has to obey. Any skill in this system can propose deviating from it for a specific piece (a reflective essay that doesn't want a closing question, a two-sentence reply that doesn't want a hook), as long as it says so and gets your go-ahead first, rather than silently deciding on its own.

---

## The core skills (11)

These work for *any* field. No persona-specific assumptions live in any of them.

**Foundation**
- **`creator-context`** — the skill everything else reads from. Captures format scope, house style, your persona (one or more fields), a generated identity/philosophy you confirm or edit, and your business profile (platforms, audience, goals). Run this first, or whenever you want to reset.

**Planning & writing**
- **`content-calendar`** — plans hooks, short captions, and long-form angles across a timeframe. Inline table by default, downloadable spreadsheet/doc on request or for longer plans.
- **`social-copywriting`** — writes the actual, publish-ready copy for a specific piece, short-form or long-form, based on your platform's format classification.

**Quality & iteration**
- **`voice-qa`** — checks a draft against your confirmed house style (banlist, punctuation, tone, formatting) and flags specific fixes. Never invents nitpicks on a clean draft.
- **`content-repurposing`** — compresses long-form into short-form, or expands short-form into long-form. Not summarizing, not padding, real structural transformation.

**Discoverability**
- **`hashtag-and-keyword`** — recommends hashtags (short-form platforms) or SEO keywords/tags (long-form platforms), generated fresh from your actual persona and the specific piece, never from a generic template.

**Research & analysis**
- **`analyse-content`** — analyzes someone else's existing content (a link, upload, or batch of several) and recommends how the underlying approach could translate into your own context. Stops at the recommendation, you decide the next step.
- **`trend-to-content`** — connects a current trend or piece of news to your specific expertise and proposes an angle, only within your genuine area of standing, and only after checking it isn't too sensitive to newsjack.
- **`content-performance-review`** — reviews your own past posts (not someone else's) and finds real, evidence-backed patterns in what's worked, evaluated against *your* stated goals, not a generic standard.

**Profile & community**
- **`bio-and-profile-optimization`** — writes or tightens a LinkedIn headline/About, Instagram bio, X bio, or a custom platform's profile field, pulled directly from your confirmed identity and philosophy.
- **`engagement-reply-drafting`** — drafts replies to comments and DMs, reading each message's type first (question, compliment, pushback, lead, spam) since each deserves different treatment.

---

## Field packs

Field packs add specialist skills that a general-purpose system can't responsibly provide, either because they need domain-specific frameworks, or because they carry risks (fabricated metrics, unconfirmed behavioral claims, undisclosed sponsorship, client confidentiality) that need field-specific handling.

Every field pack shares two baseline skills (`<field>-asset-to-content`, `<field>-content-ideation`) plus whatever specialist skills that field genuinely needs. **Every skill in a pack checks your stated field(s) in `creator-context` before running, and gives a soft warning, never a hard block, if it doesn't match.**

### Branding pack

**Brand Identity Design + Brand Strategy**, combined into one pack deliberately: in real practice, you can't defend a visual choice without the positioning work underneath it. These two disciplines aren't separable the way, say, fitness coaching and 3D animation are, so one pack serves both rather than forcing an artificial split.

| Skill | What it does |
|---|---|
| `branding-asset-to-content` | Mines an uploaded brand asset (logo grid, identity presentation, mood board, packaging mockup) into a lesson-driven post. Proposes directions and checks before drafting; never assigns meaning to a visual detail you haven't confirmed. |
| `branding-content-ideation` | Generates topic ideas from real strategy frameworks: positioning, brand architecture, competitive context, tone of voice, naming, rebrand rationale. |
| `branding-teardown` | Critiques a public brand or rebrand using real frameworks. Strictly separates confirmed facts from interpretive reads, since the subject is a real company. |
| `branding-case-study-builder` | Turns a finished project into a Challenge → Insight → Approach → Result case study. Never invents a metric you didn't provide. |
| `branding-glossary-explainer` | Explains a branding term (brand identity vs. brand image, positioning vs. messaging) for a mixed senior/junior audience. |
| `branding-confidential-story` | Helps anonymize a real client story so it's safe to share while keeping the lesson intact. Not legal advice, you're responsible for your own NDA. |

### UX pack

**UX / Product Research and Design**, spanning research, information architecture, interaction and UI design, UX engineering, AI-assisted design workflows (vibe coding), and design-to-code.

| Skill | What it does |
|---|---|
| `ux-asset-to-content` | Mines an uploaded UX asset (wireframe, user flow, research finding, IA map, design system component) into a lesson-driven post. |
| `ux-content-ideation` | Topic ideas from usability heuristics, IA, research methodology, accessibility, design systems, and AI-assisted workflows. |
| `ux-product-teardown` | Critiques a public product's UX. Requires current screenshots (UI changes fast and silently), never asserts unconfirmed user-behavior claims. |
| `ux-case-study-builder` | Challenge → Research/Insight → Design Decision → Validation/Result arc. Makes the research-to-decision link explicit, the part most case studies skip. |
| `ux-glossary-explainer` | Explains UX terms (usability vs. UX, wireframe vs. prototype, vibe coding vs. traditional prototyping). |
| `ux-tool-and-workflow-spotlight` | Reviews a specific AI design tool or workflow. Distinguishes firsthand use from general overview, resists hype, requires disclosure of any paid/affiliate relationship. |
| `ux-confidential-story` | Anonymizes a real project story, with an added category for unreleased/embargoed features. |

### Marketing pack

**Business Marketing**, kept broad on purpose, spans paid advertising, email, SEO, content marketing, and marketing strategy rather than one channel.

| Skill | What it does |
|---|---|
| `marketing-asset-to-content` | Mines an uploaded marketing asset (campaign report, ad creative, funnel diagram, analytics dashboard) into a lesson-driven post. Never invents or implies a performance number. |
| `marketing-content-ideation` | Topic ideas from funnel logic, channel strategy, attribution, positioning vs. marketing, acquisition vs. retention. |
| `marketing-campaign-teardown` | Critiques a public campaign or ad. Since real performance data almost never leaks publicly, defaults to craft-and-reasoning framing rather than assumed results. |
| `marketing-case-study-builder` | Challenge → Strategy → Execution → Result arc. Never invents a metric, and won't let a real number stand alone without context that would change how it reads. |
| `marketing-glossary-explainer` | Explains marketing terms (CAC vs. LTV, MQL vs. SQL, brand vs. performance marketing). |
| `marketing-tool-and-platform-spotlight` | Reviews a marketing tool or ad platform. Actively asks about paid/affiliate relationships rather than waiting to be told, given how normalized undisclosed sponsorship is in this content category. |
| `marketing-confidential-story` | Anonymizes a real client or campaign story, with specific figures (spend, revenue, conversion rate) treated as sensitive even without a client name attached. |

---

## How to use this system

### Core skills alone

If your field doesn't have a pack yet, or you just don't need field-specific depth, install the 11 core skills and go. Run `creator-context` once, then use whichever core skill fits: `content-calendar` to plan, `social-copywriting` to draft, `voice-qa` before you publish, and so on. Nothing about the core skills requires a field pack to function.

### Core + one field pack

The common case. Install the 11 core skills plus one pack (say, `branding/`). Run `creator-context`, listing your field as part of that pack (e.g. "brand identity designer"). From then on, Claude will recognize when to reach for a pack skill, uploading a brand asset triggers `branding-asset-to-content`, asking for a rebrand critique triggers `branding-teardown`, and so on, alongside the core skills for everything else (calendar, copywriting, QA).

### A single field-pack skill directly

You don't need to "complete" a pack in order or run every skill in it. If all you want right now is a glossary explainer, just ask for one, only that skill runs. Packs are a set of independent tools sharing one foundation, not a required sequence.

### Combining two or more field packs

If you work across disciplines (say, brand identity design *and* UX research), install both packs. When you set up `creator-context`, list every field you actually work in. The moment you list more than one, you'll be asked **one direct question, every time, regardless of how related the fields sound**: do you want these under one shared identity and voice, or should they be treated as separate contexts?

- **One shared identity**: proceed through `creator-context` once. Every pack skill you later use (from either field) reads from that same profile and voice, so a `branding-*` skill on Monday and a `ux-*` skill on Thursday sound like the same person.
- **Separate contexts**: finish the current one, then run `creator-context` again fresh (a new conversation, or an explicit reset) for the other identity, rather than trying to hold two voices in one profile.

This system never judges *for* you whether your fields are "related enough" to combine. Design disciplines and totally unrelated fields (say, fitness coaching and 3D animation) get asked the identical question. You know your own audience better than an assumption baked into a skill file ever could.

### What the mismatch warning means

Every pack skill checks your stated field(s) before running. If a `branding-*` skill is called by someone whose `creator-context` says "fitness coach," it won't refuse, it'll surface a soft warning naming the mismatch and ask if you want to proceed anyway. This is deliberate: you might have a legitimate edge case (a fitness coach who also does brand consulting on the side), and the system shouldn't assume it knows better than you do about your own work. It's a nudge, not a gate.

---

## Filling out your persona

`creator-context` will walk you through this conversationally, but here's the shape it's looking for, so you can prep your answer if you'd rather move fast:

> *"I'm a [years] [role] who specializes in [niche]. I'm known for [distinctive angle]."*
>
> *Optional, if you already have a point of view: a rough philosophy or belief about your field, jot it here and the skill will help refine it into a sharper version: [rough philosophy, if you have one]*
>
> *Optional, anything else worth knowing (how you want to come across, a reference voice, multiple fields you work across): [other]*

You don't need a polished philosophy ready. `creator-context` will generate one from what you give it and let you confirm, edit, or pick an alternate shape (declarative belief, or a "what I've learned" framing) if the default contrarian frame doesn't fit your field.

---

## Design principles behind every skill

If you're extending this system, these are the rules every skill in this repo already follows, and any contribution should too.

1. **Propose, don't assert.** Interpretive claims (what a design choice means, why a real company made a decision, what a trend implies) are hypotheses to check with the user, never facts to present unilaterally.
2. **Default with override, never silent enforcement.** House style, philosophy shape, and formatting model all ship with sensible defaults, but every one of them is presented explicitly and can be changed. A default that was never actually agreed to isn't a default, it's an assumption.
3. **Ask before assuming a blank page.** Every skill that produces content checks whether the user already has a draft, notes, or a rough idea before generating from scratch.
4. **Never invent a number.** No skill in this system fabricates a metric, a testing result, or a performance figure. If real data doesn't exist, the skill says so rather than filling the gap with something plausible-sounding.
5. **Fact vs. read, strictly separated**, especially for anything about a real, named third party (a company, a public figure, a competitor). An interpretive claim about someone else's intent or results must be framed as a read, never presented as confirmed.
6. **Field packs stay explicit.** No bundled "creative professional" or "business person" catch-all pack. Every discipline gets its own named pack. Combine two only when they're genuinely inseparable in practice (like branding's two disciplines), and even then, let the user decide, don't assume it for them.
7. **Neutral in core, specific in packs.** Core skills must never leak field-specific examples or assumptions. Pack skills, by contrast, should lean into field-specific vocabulary and examples deliberately, that's the entire point of a pack. See [CONTRIBUTING.md](CONTRIBUTING.md#the-core-vs-pack-neutrality-problem-a-real-case-study) for the actual incident that produced this rule.
8. **Disclosure is not optional where it applies.** Any skill covering tools, platforms, or products must ask about paid/affiliate relationships and require disclosure in the drafted copy itself if one exists, not just a note to the user.
9. **Confidentiality gets a dedicated, explicit skill, not a bolt-on.** Any pack involving client-facing work includes a `<field>-confidential-story` skill, and every skill that could expose client details defers to it rather than attempting a lighter anonymization pass inline.
10. **Say when something's thin.** Case studies, reviews, and analyses should call out weak or unsupported sections honestly rather than padding them to look complete.

---

## Repository structure

```
/core/<skill-name>/SKILL.md
/packs/<pack-name>/<skill-name>/SKILL.md
/README.md
/CONTRIBUTING.md   (see below)
```

Each `SKILL.md` follows the Agent Skills format: YAML frontmatter (`name`, `description`) followed by the skill's instructions in markdown. Package a skill folder as a `.skill` file (or zip it) before uploading to claude.ai.

---

## Contributing

This system is intentionally built to grow. New fields, new skills, and refinements to existing ones are all welcome. The short version of each path is below, see **[CONTRIBUTING.md](CONTRIBUTING.md)** for the full guide, including SKILL.md format requirements, a validation checklist, and the real case study behind the core-vs-pack neutrality rule.

### Updating an existing skill

Open an issue or PR describing what's not working and why. Since every skill in this system follows the [design principles](#design-principles-behind-every-skill) above, a proposed change should explain how it fits those principles, especially if it touches the propose-don't-assert discipline, the never-invent-a-number rule, or the field-match check.

### Suggesting a new skill

Before proposing a new skill, check whether it's genuinely a new capability or a variation of an existing one (a new `content-repurposing` direction, for instance, is probably not a new skill). Good candidates for new skills solve a problem no existing skill in the relevant pack (or core) currently addresses. Open an issue with:
- What the skill would do
- Why it needs to be its own skill rather than an addition to an existing one
- Whether it's core (works for any field) or pack-specific (needs a field's frameworks to be useful)

### Proposing a new field pack

This repo currently covers branding, UX/product research, and marketing. More are welcome, programming, animation, fitness, culinary, and any other field are all reasonable candidates. A new pack proposal should include:

1. **A clear field name and scope** (broad like "Business Marketing," or narrower, your call, but state it explicitly)
2. **The two baseline skills**: `<field>-asset-to-content` and `<field>-content-ideation`, adapted to what a real asset and real topic ideation look like in that field
3. **Field-specific additions**, whatever that field genuinely needs beyond the baseline. Not every pack needs the same shape, the UX and marketing packs both added a tool/platform-spotlight skill because their fields move fast and have real disclosure risk, the branding pack didn't need one. Think about your field's actual risks and content patterns rather than copying another pack's skill list by default.
4. **A `<field>-confidential-story` skill** if the field involves any client-facing or confidential work (most professional fields do)

Only combine two disciplines into one pack (the way branding did) if they're genuinely inseparable in real practice, not just adjacent. When in doubt, keep packs separate, a user can always install both.

### The one mistake to avoid

Early in this system's development, a supposedly field-neutral skill (`asset-to-content`, before it was split into packs) accidentally shipped with design-and-branding-specific examples baked into its instructions, a backend engineer or a fashion designer using it would have gotten worse results because the skill's own example vocabulary silently assumed a design context. The fix was moving field-specific language into explicit packs and keeping core skills genuinely example-neutral.

If you're contributing to a **core** skill, watch for this: any illustrative example you add should work for a random unrelated field, not just the one you happen to be thinking about while writing it. If you're contributing to a **pack**, the opposite is true, lean into field-specific examples deliberately, that's the whole value of a pack.

---

## FAQ

**Do I need every skill in a pack installed?** No. Install only the ones you'll actually use. Each skill works independently once `creator-context` is set up.

**Can I edit a skill after installing it?** Yes. On claude.ai, you can edit skill files in-chat (highlight text, "Edit with Claude") or re-upload a modified version. Since these are your files once downloaded, you can also edit the `SKILL.md` directly and re-upload.

**What happens if my field doesn't have a pack yet?** You can still use all 11 core skills fully. Field-specific skills (asset mining, teardown, case studies, glossary, tool spotlight, confidential story) simply aren't available until someone builds that pack, see [Proposing a new field pack](#proposing-a-new-field-pack) if that's you.

**Why does everything ask so many questions before producing content?** Because the alternative, confidently generating content from assumptions, is what makes AI-written content sound generic, or worse, makes it state something false about a real person, a real client, or a real result. The questions are the actual value of this system, not friction to be minimized.

**Is this affiliated with Anthropic?** No, this is a community-built set of Agent Skills for use with Claude, not an official Anthropic product.

---

## License

MIT. Use it, fork it, adapt it for your own field.
