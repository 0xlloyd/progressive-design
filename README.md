# progressive-design

A Claude skill that builds complete, bespoke design systems in a few visual rounds, so the result fits what it's for, uses what today's technology makes possible, and doesn't read as AI-made.

## What it does

- **Brief and inspirations.** One short round of questions about what the system is for, who it's for and every medium it serves (website, social content, video, slides, app, print), then it extracts only the qualities you like from your inspirations.
- **Designer-style research.** The subject's own story, a category map (breaking conventions is the default), type chosen from purpose with licence checks, colour built in OKLCH, and the art of the possible for each medium: variable fonts, wide-gamut colour, scroll-driven and view-transition animation, animated carousels and video, generative patterns, 3D and live data.
- **Design principles** that every direction is judged against.
- **Six visual rounds, ten directions each.** Direction, foundations, components, motion, imagery and voice, data and infographics. Every direction is rendered on real elements of your medium (nav, hero, footer, forms, carousel slides, live animation) with your real copy, labelled AI default or bespoke, and checked against earlier choices before you see it. Small details are derived and shown in one batch for review.
- **Update mode.** Add a new inspiration to an existing system: it adapts the qualities you want, shows a before-and-after of the whole system, and lets you explore only what changes.
- **Final check.** Contrast and grayscale on the colours that must be told apart, reduced motion, and the specimen rendered at phone, desktop and feed size.

## Outputs

- `tokens.json` in the W3C Design Tokens format (2025.10), importable with Tokens Studio, Style Dictionary or Terrazzo
- `DESIGN.md` guide with principles, rules and reasons, and a full decision log
- `specimen.html` showing every component in use with your real copy and motion running live
- A Claude Design System artifact, where available

## Install

Copy the `progressive-design-system/` folder into your skills directory (for Claude Code, `~/.claude/skills/`), or zip it and upload it as a skill in Claude.

## Use

Ask for a design system, brand system or visual identity, or share an inspiration with your existing DESIGN.md. For example:

> I'm launching a small ceramics studio and need a visual identity: colours, fonts, the lot.

## Contents

```
progressive-design-system/
├── SKILL.md
├── references/
│   ├── research-standard.md   eight criteria for designer research, incl. the art of the possible
│   ├── ai-defaults.md         common AI defaults, used to label options
│   └── decision-map.md        the six rounds and their decisions, with modules per medium
├── assets/
│   ├── tokens.json            W3C token skeleton
│   ├── DESIGN.md              guide and decision-log template
│   └── specimen.html          specimen page shell
└── scripts/
    └── color_check.py         WCAG/APCA contrast, gamut, grayscale for colours that must be told apart, OKLCH ramps (standard library only)
```

`color_check.py` examples:

```
python3 scripts/color_check.py pair "#5a3e2b" "#f4efe6"
python3 scripts/color_check.py ramp 40 0.14
python3 scripts/color_check.py tokens tokens.json
```

The skill ends each session by running `session-self-learning` if it's installed, so it keeps improving from real use.
