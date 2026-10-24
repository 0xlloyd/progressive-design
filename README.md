# progressive-design

A Claude skill that builds bespoke design systems one decision at a time, so the result fits what it's for and doesn't read as AI-made.

## What it does

- **Brief and inspirations.** Asks what the system is for, who it's for and where it lives, then extracts only the layers you like from your inspirations (websites, screenshots, photos, anything).
- **Designer-style research.** Researches the subject's own story, maps the category, chooses type from purpose (with licence and language checks) and builds colour in OKLCH with contrast checked as it goes.
- **Design principles.** Agrees three to five principles that every later option is judged against.
- **One decision at a time.** Five options per decision (more on request), each labelled **AI default** or **bespoke** and traced to the brief, an inspiration or a research finding. AI defaults aren't banned, just made visible.
- **Update mode.** Add a new inspiration to an existing system: it adapts the qualities you want rather than copying them, then re-checks every decision for impact.

## Outputs

- `tokens.json` in the W3C Design Tokens format (2025.10), importable with Tokens Studio, Style Dictionary or Terrazzo
- `DESIGN.md` guide with principles, rules and reasons, and a full decision log
- `specimen.html` showing the system with your real copy
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
│   ├── research-standard.md   seven criteria for designer research
│   ├── ai-defaults.md         common AI defaults, used to label options
│   └── decision-map.md        every decision per layer, in order
├── assets/
│   ├── tokens.json            W3C token skeleton
│   ├── DESIGN.md              guide and decision-log template
│   └── specimen.html          specimen page shell
└── scripts/
    └── color_check.py         WCAG/APCA contrast, gamut, grayscale and OKLCH ramps (standard library only)
```

`color_check.py` examples:

```
python3 scripts/color_check.py pair "#5a3e2b" "#f4efe6"
python3 scripts/color_check.py ramp 40 0.14
python3 scripts/color_check.py tokens tokens.json
```

The skill ends each session by running `session-self-learning` if it's installed, so it keeps improving from real use.
