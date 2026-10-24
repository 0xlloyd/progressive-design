# Decision map

Work through these decisions in order. Each one lists what is decided, what it depends on and the tokens it produces, so the decision loop covers the whole system and update mode can re-check every decision.
Skip a decision only when the brief makes it irrelevant (for example, no data visualisation), and mark it "not needed" in the decision log rather than leaving it out.

## Contents

1. Foundations: colour
2. Foundations: typography
3. Foundations: space and layout
4. Foundations: shape and elevation
5. Components
6. Motion and interaction
7. Imagery and voice
8. Layers from inspirations

## 1. Foundations: colour

| ID | Decision | Depends on | Tokens |
|---|---|---|---|
| C1 | Colour strategy: how much colour the system uses (mostly neutral with one accent, two-colour, full palette) | Principles, category map | none (recorded in DESIGN.md) |
| C2 | Primary brand colour | C1 | `color.brand.primary` |
| C3 | Neutral family: warm, cool or tinted toward the primary | C2 | `color.neutral.*` |
| C4 | Neutral ramp: number of steps and lightness spacing | C3, medium | `color.neutral.50`–`950` |
| C5 | Secondary or accent colours, if any | C1, C2 | `color.brand.secondary`, `color.brand.accent` |
| C6 | Ramps for brand colours | C2, C5 | `color.brand.<name>.50`–`950` |
| C7 | Semantic roles: background, surface, text, muted text, border, focus | C4, C6 | `color.bg`, `color.surface`, `color.text`, `color.text-muted`, `color.border`, `color.focus` |
| C8 | Status colours: success, warning, error, info, tuned to the palette | C2, C3 | `color.status.*` |
| C9 | Dark mode: whether, and how roles map | C7, medium | `color.*` dark set |
| C10 | Data visualisation palette, if needed | C6, C8 | `color.data.*` |

## 2. Foundations: typography

| ID | Decision | Depends on | Tokens |
|---|---|---|---|
| T1 | Type strategy: one family, a pair, or a superfamily | Principles, brief | none |
| T2 | Display or headline face | T1, subject story | `font.family.display` |
| T3 | Text or body face | T2 | `font.family.text` |
| T4 | Data or code face, if needed | T3 | `font.family.mono` |
| T5 | Type scale: base size and ratio, tested in real copy | T2, T3, medium | `font.size.*` |
| T6 | Weights in use and what each is for | T2–T4 | `font.weight.*` |
| T7 | Line height and letter-spacing per size | T5 | `font.lineHeight.*`, `font.letterSpacing.*` |
| T8 | Text styles: heading levels, body, caption, label, numerals | T5–T7 | `typography.*` composites |
| T9 | Typographic details: numerals (tabular or proportional), case, measure (line length) | T8 | recorded in DESIGN.md |

## 3. Foundations: space and layout

| ID | Decision | Depends on | Tokens |
|---|---|---|---|
| S1 | Density: compact, comfortable or airy | Principles, medium | none |
| S2 | Base unit and spacing scale | S1, T5 | `space.*` |
| S3 | Grid: columns, gutters, margins, max width | S2, medium | `layout.*` |
| S4 | Breakpoints, if screen-based | S3 | `breakpoint.*` |
| S5 | Layout character: symmetry, alignment, how sections are composed | Principles, category map | recorded in DESIGN.md |

## 4. Foundations: shape and elevation

| ID | Decision | Depends on | Tokens |
|---|---|---|---|
| E1 | Corner radius scale (including square, if chosen) | Principles, inspirations | `radius.*` |
| E2 | Border weights and styles | E1, C7 | `border.*` |
| E3 | Elevation approach: shadows, tonal layers, borders or none | E2, C9 | `shadow.*` or `color.surface.*` |
| E4 | Texture or surface treatment, if any (grain, paper, pattern) | Inspirations | recorded in DESIGN.md, assets |

## 5. Components

Decide the shared character first, then each component in the order the user needs them. For each component, decide anatomy, variants, states (default, hover, focus, active, disabled, error, loading) and the tokens it uses.

| ID | Decision | Depends on |
|---|---|---|
| K1 | Component character: how foundations combine (for example flat and bordered, or solid and filled) | Foundations |
| K2 | Buttons and links | K1 |
| K3 | Form inputs: text fields, selects, checkboxes, radios, toggles | K1 |
| K4 | Cards and containers | K1, E3 |
| K5 | Navigation: header, menus, tabs, breadcrumbs | K1, S3 |
| K6 | Feedback: alerts, toasts, empty states, loading | K1, C8 |
| K7 | Data display: tables, lists, tags, badges, charts | K1, T9, C10 |
| K8 | Overlays: modals, drawers, tooltips | K1, E3 |
| K9 | Any components specific to the product | K1 |

## 6. Motion and interaction

| ID | Decision | Depends on | Tokens |
|---|---|---|---|
| M1 | Motion character: none, subtle, expressive | Principles | none |
| M2 | Duration scale | M1 | `duration.*` |
| M3 | Easing curves and what each is for | M1 | `easing.*` (cubicBezier) |
| M4 | State changes: hover, press, focus style | M2, M3, C7 | recorded in DESIGN.md |
| M5 | Transitions and entrances: what moves, what never moves | M1 | recorded in DESIGN.md |
| M6 | Reduced-motion behaviour | M5 | recorded in DESIGN.md |

## 7. Imagery and voice

| ID | Decision | Depends on |
|---|---|---|
| I1 | Photography style, if used: subject, light, framing, treatment | Principles, subject story |
| I2 | Illustration style, if used | Principles, inspirations |
| I3 | Iconography: style, stroke, corner, grid, source | E1, T6 |
| I4 | Graphic devices: patterns, shapes, motifs drawn from the subject | Subject story |
| I5 | Voice: personality, vocabulary, words to use and avoid | Brief, category map |
| I6 | Copy patterns: headlines, buttons, errors, empty states | I5 |

## 8. Layers from inspirations

Add one row per layer the user accepted from an inspiration (for example a grid system, texture or illustration language). For each, decide what it is, where it applies, the rules and the tokens or assets it needs, and record its source inspiration.
