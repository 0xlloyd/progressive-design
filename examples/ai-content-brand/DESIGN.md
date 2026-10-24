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

1. **[Principle]:** [the choice the system makes] — [what it gives up].
2. …

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
[Layers accepted from inspirations, each with rules and source.]

## 9. Using the system in other tools
- **Code:** import `tokens.json` with a token tool such as Style Dictionary or Terrazzo to generate CSS variables or platform code.
- **Design tools:** import `tokens.json` with a token plugin such as Tokens Studio.
- **AI tools:** give them this file and `tokens.json`, and ask them to follow the rules and their reasons.

## 10. Decision log

| ID | Decision | Choice | Label | Source | Principle | User's reason | Date |
|---|---|---|---|---|---|---|---|
| C2 | Primary brand colour | [value] | bespoke / AI default | [brief, inspiration or research] | [principle] | [reason, if given, or "delegated"] | [date] |

## 11. Not yet decided
- [Decision IDs and layers still open]

## 12. Inspirations and changelog
| Date | Change | Inspiration | Decisions affected |
|---|---|---|---|
| [date] | System created | [inspirations used] | All |
