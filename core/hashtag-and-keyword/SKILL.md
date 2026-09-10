---
name: hashtag-and-keyword
description: Recommends hashtags for post-format platforms (X, Threads, Instagram/TikTok, Facebook, LinkedIn Standard Post) and SEO keywords/tags for true long-form article platforms (LinkedIn Article, Medium, Substack), based on the user's actual persona, niche, and the specific piece of content, never invented from a generic template. Use whenever the user asks for hashtags, tags, keywords, wants help with discoverability, asks "what hashtags should I use," or wants a piece optimized to be found on a platform. Requires creator-context to be active for persona, profile, and platform tiers.
---

# Hashtag and Keyword

Recommends discoverability terms, hashtags for short-form platforms, SEO keywords and tags for long-form platforms, grounded in the user's actual field and the specific piece of content, not generic terms invented from a template. This skill has no built-in examples of "good hashtags for your field," it generates them fresh from the user's real persona and the real content every time.

## Before recommending

Confirm `creator-context` is active for persona, niche, and platform tiers/character limits. This skill leans on the persona more than most others in this system, generic terms are the main failure mode to avoid here (see below), so don't proceed without knowing the user's actual field and specialization.

Get the actual piece of content the tags are for, pasted text, an uploaded draft, or something produced earlier in the conversation. Tags generated without seeing the actual content tend toward generic field-level terms rather than terms that match what this specific piece is actually about.

## Which behavior applies: hashtags or SEO keywords

This system classifies platforms into three length tiers (short-form, platform-native long post, true long-form article) for writing purposes, but discoverability behavior doesn't split the same way. It splits on **post vs. article**, since that's what actually determines how content gets found:

- **Hashtag behavior** applies to every platform in the short-form tier *and* the platform-native long post tier, X, Threads, Instagram/TikTok Story captions and main captions, Facebook, and LinkedIn Standard Post. All of these are discovered primarily through in-platform social and algorithmic mechanisms, hashtags included, not through general web search, regardless of how long the post itself is allowed to run.
- **SEO keyword behavior** applies only to the true long-form article tier, LinkedIn Article, Medium, Substack. These get indexed and found through actual search, so the mechanism is genuinely different, not just "long hashtag behavior."

If the target is LinkedIn, confirm which format: a LinkedIn Standard Post uses hashtag behavior, a LinkedIn Article uses SEO keyword behavior, same platform, different mechanism, don't assume based on the platform name alone.

## Why genericness is the main risk here

Unlike most of this system's skills, this one has to generate example terms to be useful at all, and terms are exactly where a generic template leaks a specific field's assumptions into every use case (the way "brand identity," "logo grid," "UX wireframe" leaked into an earlier version of a different skill in this system). A backend engineer asking for hashtags should get terms like their actual specialization suggests, not repurposed design or marketing hashtags. Every term recommended here should trace back to something in the user's stated persona/niche or the content itself, not to this skill's own assumptions about what hashtags "usually" look like.

## Hashtag behavior (short-form and platform-native long post tiers)

- Pull terms from three tiers, and generate real examples for each tier at the time of the request, using the user's actual field, niche, and the specific post, don't reuse terms from a previous user's session or a built-in list:
  - **Broad/high-volume**: terms with wide reach in the user's general field
  - **Niche/specific**: terms matching the user's exact specialization, smaller audience, higher relevance
  - **Community/branded**: terms tied to the user's own account, a recurring series, or a community they're part of, if applicable
- Recommend a reasonable count for the specific platform, not a one-size-fits-all number, Instagram tolerates more tags than X, LinkedIn Standard Posts typically read better with fewer, more targeted tags than Instagram does, Facebook hashtags carry less discoverability weight than on the other platforms. Say why that count for that platform, rather than just listing a number without explanation.
- Present the recommendation as a proposed set, not a final list, ask if any feel off-target or if the user wants more weight toward broad reach vs. niche relevance

## SEO keyword behavior (true long-form article tier only)

- Identify the core search terms someone might actually type to find content like this, grounded in the piece's real topic and the user's niche
- Distinguish between **platform tags** (Medium/Substack-style topic tags, usually a handful, chosen from how the platform categorizes content) and **in-text keyword presence** (terms worth naturally appearing in the title, opening lines, or subheadings for searchability), these are different mechanisms and shouldn't be conflated
- Don't recommend keyword stuffing, forcing terms into the piece unnaturally undermines the house style and reads as compliance-driven rather than genuinely written

## Presenting the recommendation

Present it as a clearly labeled set (broad/niche/community for hashtag behavior, tags/keywords for SEO keyword behavior), with a one-line reason for each category, not just a bare list. Invite the user to swap out anything that doesn't fit, they know their actual audience and community better than a generated guess does.

## Scope

This skill doesn't guarantee reach or algorithm performance, it recommends relevant, well-targeted terms based on what's knowable from the content and persona. Don't imply guaranteed outcomes ("this will get you more views"), frame recommendations as relevance-based, not performance-guaranteed.
