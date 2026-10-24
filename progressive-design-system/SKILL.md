---
name: progressive-design-system
description: "Build or update a bespoke design system one decision at a time, from the user's brief, inspirations and designer-style research, so it fits what it's for and doesn't read as AI-made. Use when the user wants to create a design system, brand system or visual identity, or to add a new inspiration (a website, image or screenshot) to an existing design system, even if they don't say \"design system\". Produces design tokens in the W3C format, a DESIGN.md guide, a visual specimen page and, where available, a Claude Design System artifact, so the system works in any tool."
---

# Progressive Design System

## Purpose

This skill keeps the user as the designer: it researches, proposes options and records decisions, but nothing enters the design system until the user has chosen it.
Left to themselves, AI tools pick the statistical average of what they've seen (Inter, purple–indigo gradients, a centred hero with three rounded cards), and asking them to avoid it just shifts them to the next most common choice, such as warm cream with a terracotta accent.
So instead of banning those defaults, the skill labels every option as AI default or bespoke and traces each bespoke option to the brief or an inspiration, because a default can still be the right choice when the user picks it knowingly.

## Modes

Start by asking whether the user is creating a new design system or updating an existing one with a new inspiration, and for an update, ask for the existing system's files (tokens, DESIGN.md or a link) before anything else.
If the request already makes the mode clear, such as the user sharing a new inspiration alongside their DESIGN.md, skip the question and say which mode you're in.
A new system runs every section below in order, while an update reads the existing files first and then follows Update mode.

## Brief

Ask what the design system is for, who it's for, where it will live (web, app, print, slides or several), the feeling it should give, any constraints such as existing logos, brand colours, budget for paid fonts or accessibility targets, and the real copy it will carry, such as a headline and a paragraph.
Ask a few questions at a time rather than all at once, take any answers already in the conversation, and if the user has no real copy yet, offer to draft some, because type and colour choices tested on placeholder text hide real problems.
Play the answers back as a short brief and get the user's confirmation, since every later option is judged against it.

## Inspirations

Invite the user to share anything they like the look or feel of, such as websites, screenshots, photos, packaging, posters or places, and say that inspirations from outside design galleries often give the most distinctive results.
For each inspiration, extract the usable elements layer by layer (colours with values, typefaces or their closest match, spacing and density, shapes and corners, imagery, motion and tone of voice) and tag each one with the inspiration it came from.
Ask the user which layers drew them to each inspiration, such as "just the colour" or "the type and the spacing", and keep only those, because an inspiration is a source of qualities to adapt, not a design to copy.
When a website can't be reached, ask the user for screenshots instead, and when a typeface can't be identified with confidence, say so and offer the closest matches rather than guessing.
If an inspiration brings a quality the standard layers don't cover, such as a paper texture, an unusual grid or an illustration style, propose it as a new layer the user can accept or skip.

## Research

Before proposing any options, research the way a senior designer would, following the seven criteria in `references/research-standard.md`: the subject's own story, the category, type chosen from purpose, pairing rationale, colour built for the medium, practical fitness and provenance.
Start with the subject's own story (its history, place, era, materials and audience), because that's where the options nobody else can copy come from.
Then map four to eight others in the same category on colour, type, imagery and layout, name the conventions they share, and ask the user whether to follow those conventions or break them, since experts disagree and it depends on how much the brand can back up being different.
For type, search foundries and libraries beyond the most popular (for example Google Fonts, Fontshare and independent foundries), and note each candidate's licence, language coverage and weights before it becomes an option.
For colour, work in OKLCH (a colour space where equal steps look equally different to the eye) and check each candidate with `scripts/color_check.py` for contrast, gamut and grayscale in the user's medium, because colours picked by eye and checked later often fail or look muddy once fixed.
Share the findings as a short summary with sources, covering the subject's story, the category map and any early type and colour directions, and get the user's reactions before moving on.
If web search isn't available, research from what you already know and tell the user which facts need checking, especially font licences, since those change and matter legally.

## Design principles

From the brief, inspirations and research, propose three to five design principles, each a short statement of a choice the system makes and what it gives up, such as "Dense over airy: show more data per screen, even if it feels less calm".
Revise them until the user approves them, then use them as the yardstick for every later option, saying which principle each option serves.

## Decision loop

Work through the decisions in `references/decision-map.md` one at a time, in its order, because each choice narrows the next and a system built decision by decision stays coherent.
For each decision, show five options by default and more when the user asks, making sure at least one is the AI default (checked against `references/ai-defaults.md`) so the user can see what they'd get without the skill.
Give each option a label (AI default or bespoke), its source (the brief, a named inspiration or a research finding), the principle it serves, a one-line rationale, and the practical facts that apply, such as contrast results, licence or language coverage.
Show options visually wherever the environment allows, such as colour swatches or type samples set in the user's real copy, because design choices are hard to judge from names and hex codes alone.
Let the user pick one, mix parts of several, edit an option or ask for more, and if none fit, ask what's missing before generating new ones rather than guessing again.
If the user asks you to decide something for them, choose the option that best serves the principles, record it as "delegated" in the decision log, and move on, so they can revisit it later.
Record each choice in the decision log as soon as it's made (the decision, the option chosen, its label, source and the user's reason if they gave one), so the work survives an interrupted session and update mode can re-check it later.
Keep the decision log in the user's DESIGN.md, started from `assets/DESIGN.md`, and after each layer is finished, update the specimen page so the user sees the system come together as a whole.
If a choice clashes with an earlier one, such as a new accent that fails contrast on the chosen background, say so straight away and let the user decide which to change.

## Layer order

Build the layers in this order: foundations (colour, type, spacing, shape, elevation), then components, then motion and interaction, then imagery and voice, then any layers the user accepted from inspirations, because each layer is built from the ones before it.
If the user only needs some layers, such as foundations for a slide template, build those and mark the rest as not yet decided in DESIGN.md, so a later session can pick them up.

## Update mode

Read the existing DESIGN.md, tokens and decision log first, so you know every decision already made, its source and the principles behind it.
Extract only the layers the user says drew them to the new inspiration, and adapt those qualities to the existing system rather than copying them in, for example taking an inspiration's warmth by shifting the existing palette's hue rather than replacing it with the inspiration's colours.
Then re-run every decision in the decision map against the adapted qualities, not just the obvious ones, and for each show "keep" or "change" with the reason, because a new colour can quietly break contrast, states or imagery elsewhere in the system.
For every "change", run the normal decision loop with five options, including keeping the current choice, and for "keep" decisions, let the user confirm them in one batch so the update doesn't drag.
If the new inspiration conflicts with an approved design principle, point this out and ask whether to adapt the inspiration further or revise the principle, rather than letting the system drift.
If the existing system wasn't built with this skill and has no decision log, rebuild one from its tokens and guide, mark each decision's source as unknown, and confirm the reconstruction with the user before re-running anything.
Add the inspiration and every change it caused to the decision log with the date, so the system's history shows why it looks the way it does.

## Outputs

Produce four outputs from the same decisions, so they never disagree: design tokens in the W3C Design Tokens format (2025.10), started from `assets/tokens.json`; the DESIGN.md guide with principles, rules, do's and don'ts and the decision log; a specimen page built from `assets/specimen.html` that shows the system with the user's real copy; and a Claude Design System artifact where that artifact type is available.
Write DESIGN.md so another person or AI tool can apply the system without this conversation, stating each rule with its reason, because a rule without a reason gets broken the first time it's inconvenient.
If the Claude Design System artifact type isn't available, deliver the other three and tell the user the tokens file can be imported into design tools and code through token tools such as Tokens Studio or Style Dictionary.

## Final check

Before delivering, run `scripts/color_check.py` on every text and background pair in the tokens, flag anything that fails contrast for the user's medium with two or three fixes to choose from, and confirm the system still reads clearly in grayscale.
Then show the user how many of their choices are AI defaults and which ones, not as a warning but so they can confirm each was deliberate, and check the four outputs match each other.

## Close

End by running `session-self-learning` on this skill so lessons from the session improve the next one; if that skill isn't installed, suggest any improvements to this skill directly for the user to approve.
