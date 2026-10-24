# AI content brand design system

> Version 0.1.0 · Updated 2026-10-24
> Tokens: `tokens.json` (W3C Design Tokens format 2025.10) · Specimen: `specimen.html`

This guide lets any person or tool apply the system without the conversation that created it. Every rule states its reason, so it can be applied with judgement.

## 1. Brief

- **What it's for:** a professional brand for AI content.
- **Who it's for:** AI builders, and people already using AI who want to use it more and better.
- **Where it lives:** mainly LinkedIn (carousels as PDF documents, single-image posts, profile banner and photo treatment); later slides and a personal site.
- **Feeling:** excited, inspired, cool, useful, valuable.
- **Constraints:** clean start with no carry-over from any previous look; free fonts only; WCAG AA contrast minimum, since LinkedIn is read mostly on phones, often in bright light.
- **Real copy used for testing:**
  - Hook: "I gave Claude my worst Monday and got three hours back."
  - Paragraph: "I feel very strongly that most people are using AI like a search box. And so this week I handed it the whole workflow, from the meeting notes to the follow-up emails, and essentially let it run the first draft of my day. You can think about it as a junior teammate who never gets tired, and the trick is giving it the context you'd give a person."
  - Carousel slide: "Step 2 · Give it the context you'd give a teammate"
  - Stat line: "3 hours saved · 12 emails drafted · 1 prompt"

## 2. Design principles

1. **Built, not imagined:** show real artefacts (files, steps, data, the actual workflow) instead of robots, brains and glow. Gives up the instant "this is about AI" signal.
2. **Stand out from the feed:** colours that differ from LinkedIn's own in both light and dark mode. Gives up the soft off-white look.
3. **One idea, one glance:** every slide carries one point, made visible with a mini chart or visual where it helps. Gives up dense, text-heavy slides.
4. **Face first:** the author is visible on every piece (headshot and name), because people follow people. Gives up a fully anonymous editorial look.
5. **Excited, not hyped:** energy comes from colour, scale and contrast, never from hype words, emoji or all caps. Gives up the cheap scroll-stoppers.

## 3. Research summary

- **Subject's story:** builder culture (the "0x" hex prefix, monospace, terminal); building in the open with real artefacts (files, steps, workflows); a conviction about owning your context across tools (nodes, links, flows). The London insurance market angle was considered and dropped by the user.
- **Category conventions (AI creators on LinkedIn):** dark slides with purple or blue gradients and glow; Inter, Montserrat or Poppins from carousel templates; LinkedIn-blue accents; chat screenshots, emoji bullets, 3D robots and brains; headshot and name on every slide.
- **Position:** break the conventions (user's call). The headshot stays only because it comes from the user's own inspiration (the one-pager header), not as a convention.
- **Medium findings:** carousels are PDFs at 1080 x 1350 (4:5), usually 6 to 14 slides. LinkedIn's light feed is #F4F2EE and its dark mode is #1B1F23, so off-white or pure black bases blend into the feed; a tinted or coloured base stands out in both. Avoid LinkedIn blue #0A66C2 as the main accent. Body text needs roughly 36px or more on a 1080px slide to read on a phone.
- **Inspirations:** Elementor website (fonts and colours: heavy friendly grotesk, black and off-white with hot pink #ED01EE, burgundy #620856 / #2A0624, lilac #E5C0FF, acid lime #D5FF45, deep green #00452E). One-pager infographic (header with headline and circular headshot, problem/fix table layout, mini charts and infographic visuals).
- **Sources:** https://styles.refero.design/style/4bbc63cf-c995-4c56-9873-e7f300f1c9e7 · https://elementor.com/logos/ · https://ruben.substack.com/p/carousels · https://www.oppadu.com/tools/design-systems-site/brand/linkedin.html · https://madegooddesigns.com/free-commercial-use-fonts/

## 4. Foundations

### Colour
[Strategy in one line. Table of roles with OKLCH and hex values, and what each role is for.]
- **Do:** [rule] — [reason]
- **Don't:** [rule] — [reason]
- **Contrast:** [tested pairs and results]

### Typography
[Faces, licences and why they pair. Scale table with sizes, line heights and uses.]
- **Do / Don't:** [rules with reasons]

### Space and layout
[Density, base unit, scale, grid, breakpoints, layout character.]

### Shape and elevation
[Radius scale, borders, elevation approach, any texture.]

## 5. Components
[For each component: anatomy, variants, states, tokens used, do's and don'ts.]

## 6. Motion and interaction
[Character, durations, easing, state changes, what never moves, reduced-motion behaviour.]

## 7. Imagery and voice
[Photography, illustration, icons, graphic devices, voice, words to use and avoid, copy patterns.]

## 8. Additional layers
- **Infographic language** (accepted 2026-10-24, from the one-pager inspiration): a reusable kit of mini charts, dot grids and icon groups. Rules to be decided after imagery and voice.
- **Graph-paper grid** (accepted 2026-10-24, from the one-pager inspiration): a faint grid behind content. Rules to be decided after imagery and voice.

## 9. Using the system in other tools
- **Code:** import `tokens.json` with a token tool such as Style Dictionary or Terrazzo to generate CSS variables or platform code.
- **Design tools:** import `tokens.json` with a token plugin such as Tokens Studio.
- **AI tools:** give them this file and `tokens.json`, and ask them to follow the rules and their reasons.

## 10. Decision log

| ID | Decision | Choice | Label | Source | Principle | User's reason | Date |
|---|---|---|---|---|---|---|---|
| C1 | Colour strategy | Pop pastels in two roles: pastel backgrounds for covers and section slides; black and white with pastel accents for content slides. Palette direction: coral #FFB3A3, butter #FFE58F, lilac #D9C8FF, with black ink | bespoke | Elementor screenshots (black and white base, small pastel pops), Elementor lilac, butter from tile pop option | 2 Stand out from the feed; 5 Excited, not hyped | Preferred pop pastels over the darker and louder first-round options; chose option 10 of three rounds | 2026-10-24 |
| C2 | Primary brand colour | Coral #FFB3A3 (oklch 0.83 0.09 30) as signature: banner, profile treatment and most covers; butter and lilac support | bespoke | Chosen palette (C1) | 2 Stand out from the feed; 5 Excited, not hyped | Picked coral signature over butter, lilac, black-only and the indigo default | 2026-10-24 |
| C3 | Neutral family | Warm paper: background #FAF6EC, border #E6DFCF, muted text #6B6152 (5.6:1 on background), ink #1A1712 | bespoke (resembles the warm-cream "less AI" default, flagged and chosen knowingly) | Butter in the chosen palette | 5 Excited, not hyped (warmth); content slides only, so principle 2 is unaffected | Picked option 6 from two rounds of neutrals | 2026-10-24 |
| C4 | Neutral ramp | Light-heavy nine steps: #FFFAEE, #FAF6EC, #F2EADB, #E6DFCF, #D7D0C1, #A39E92, #6B6152, #3D3A34, #1A1712 | bespoke | Built around the C3 tones in OKLCH (hue ~86) | 3 One idea, one glance (layered cards and pastel charts) | Picked the light-heavy ramp | 2026-10-24 |
| C5 | Supporting colour roles | Butter #FFE58F is the highlighter for key words and numbers (ink on butter 14:1); lilac #D9C8FF handles secondary covers and charts; deep coral #BC4C31 for emphasis words and numbers in headings and short phrases (4.6:1 on paper, not for body text) | bespoke | Chosen palette; pastels can't carry text, so a deep coral was added | 3 One idea, one glance; 5 Excited, not hyped | Combined options 3 and 5 | 2026-10-24 |
| C6 | Brand colour ramps | Six OKLCH steps each (tint, pastel, mid, deep, darker, ink). Coral #FFEDE9 #FFB3A3 #E68774 #BC4C31 #703D33 #3E1F18; butter #FAF2D5 #FFE58F #C3A118 #8C7200 #5D4B00 #332800; lilac #F3EFFF #D9C8FF #AD97DB #7D66A7 #52456A #2C243B | bespoke | Built from the exact C1/C2 pastels and the C5 deep coral | 3 One idea, one glance (enough steps for charts) | Picked six-step ramps | 2026-10-24 |
| C7 | Semantic roles | Page: paper #FAF6EC by default; white #FFFFFF page variant for data-heavy or infographic slides (cards switch to paper #FAF6EC). Cards: #FFFAEE with hairline #E6DFCF for everyday content; ink-outlined (1.5px #1A1712) for the single key takeaway, checklist or fix. Text: ink #1A1712, muted #6B6152, deep coral #BC4C31 for emphasis, butter #FFE58F highlight | bespoke | Combination of options 2, 3 and 5; ink outline from Elementor's black and white edge | 3 One idea, one glance (the ink outline always marks the one idea) | Wanted both page colours and both card styles, with clear jobs | 2026-10-24 |
| C8 | Status colours (good versus bad) | No status hues. "Before" or "bad": muted hairline card with muted text. "After" or "good": ink-outlined card with butter highlight on the winning phrase. Symbols optional | bespoke | Reuses C5 highlighter and C7 outline | 3 One idea, one glance; 5 Excited, not hyped | Picked option 5; avoids a "bad" rose sitting next to the coral signature | 2026-10-24 |
| C9 | Dark slides | No dark slides for LinkedIn; always light. Revisit dark mode when a website or talks need it | bespoke | LinkedIn shows images as designed in both feed modes | 3 One idea, one glance (simplicity) | Picked option 2 | 2026-10-24 |
| C10 | Chart palette | Coral #FFB3A3 for the one value that matters; every other series in paper grey #D7D0C1; gridlines and axes #D7D0C1 | bespoke | Principle 3 and the C1/C4 choices | 3 One idea, one glance | Picked option 2 | 2026-10-24 |
| T1 | Type strategy | One characterful grotesk family for everything; weight contrast does the work (heavy headlines, regular body). No monospace | bespoke | Elementor uses one family (Roobert) throughout | 3 One idea, one glance; 5 Excited, not hyped | Picked option 2; earlier disliked monospace for stats | 2026-10-24 |
| T2 | Type family | Onest (Google Fonts, SIL Open Font License, weights 100–900, wide language coverage) for display and text | bespoke | Research: free faces with Roobert's qualities; most readable at phone size | 3 One idea, one glance; 4 Face first (clear, human) | Picked Onest over Schibsted, Gabarito, Rethink and the Plus Jakarta default | 2026-10-24 |
| T3 | Text face | Onest (same family, per T1) | bespoke | T1 | 3 One idea, one glance | Follows from T1 | 2026-10-24 |
| T4 | Data or code face | Not needed: numerals set in Onest; monospace disliked | bespoke | User feedback on C1 previews | 3 One idea, one glance | User disliked monospace for stats | 2026-10-24 |
| T5 | Type scale | Poster scale, ratio about 1.618, on a 1080 x 1350 slide: label 32, body 42, subhead 68, headline 110, poster headline 136. Nothing below 32px, so text stays readable at phone size | bespoke | Research: phones show a 1080px slide at about a third of its size | 3 One idea, one glance; 5 Excited, not hyped | Picked the poster scale | 2026-10-24 |
| T6 | Weights | Two weights: 400 for body, labels and captions; 900 for headlines, stats and names. Emphasis inside body uses colour or butter highlight, not a third weight | bespoke | Elementor's 900-weight headlines | 5 Excited, not hyped (energy from contrast) | Picked option 2 | 2026-10-24 |
| T7 | Line height and letter-spacing | Headlines: line height 1.05, letter-spacing -1.5%. Body and labels: line height 1.45, letter-spacing 0 | bespoke | Gentler version of Elementor's tight headlines | 4 Face first (approachable); 5 Excited, not hyped | Picked "Friendly" | 2026-10-24 |
| T8 | Text styles | Poster headline 136/900, headline 110/900, subhead 68/900, body 42/400, label 32/400 muted, stat 900, name line 32 (name 900, role 400). Step slides lead with a big numeral (200/900) in deep coral #BC4C31 (4.6:1 on paper) | bespoke | One-pager numbered rows; deep coral from C5 | 3 One idea, one glance; 2 Stand out from the feed (signature colour on content slides) | Picked the big coral numeral, then deep coral to resolve a clash with the C5 rule that pastels are never text | 2026-10-24 |

## 11. Not yet decided
- Dark mode (C9): revisit for a website or talks.

## 12. Inspirations and changelog
| Date | Change | Inspiration | Decisions affected |
|---|---|---|---|
| [date] | System created | [inspirations used] | All |
