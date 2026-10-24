# AI content brand design system

> Version 1.0.0 · Updated 2026-10-24
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

All sizes are in pixels on a 1080 x 1350 slide (LinkedIn's 4:5 carousel page) unless noted. Phones show that slide at about a third of its size, so every rule is written for that.

### Colour

Pop pastels in two roles: pastel backgrounds for covers and section slides; warm paper with pastel accents for content slides. Coral is the signature.

| Role | Token | Value | Use |
|---|---|---|---|
| Signature | `color.brand.coral.200` | #FFB3A3 · oklch(0.835 0.092 32) | Covers, banner, the one value in a chart |
| Highlighter | `color.brand.butter.200` | #FFE58F · oklch(0.925 0.110 93) | Key words and numbers; ink on butter 14.3:1 |
| Support | `color.brand.lilac.200` | #D9C8FF · oklch(0.865 0.077 299) | Secondary covers |
| Emphasis | `color.brand.coral.600` | #BC4C31 | Emphasis words in headings and step numerals; 4.6:1 on paper, never body text |
| Page | `color.bg` | #FAF6EC | Default content background |
| Page, data | `color.bg-data` | #FFFFFF | Data-heavy and infographic slides; cards switch to paper |
| Card | `color.card` | #FFFAEE | Everyday cards, with `color.border` hairline |
| Border | `color.border` | #E6DFCF | Hairlines and dividers |
| Text | `color.text` | #1A1712 | All text; 16.6:1 on paper, 10.4:1 on coral |
| Muted text | `color.text-muted` | #6B6152 | Labels and secondary text; 5.6:1 on paper |
| Chart other | `color.data.other` | #D7D0C1 | Every chart series except the one that matters |
| Grid line | `color.grid` | #E3DACA | Graph-paper grid only |

- **Do:** give every cover a pastel background, because only the cover appears in the feed and LinkedIn's own feed is warm off-white (#F4F2EE) or neutral dark (#1B1F23), so pastels stand out in both modes.
- **Do:** rotate covers across coral (most), butter and lilac, because coral should be the colour people remember while a series still feels varied.
- **Don't:** set text in a pastel, because pastels are 1.2–1.6:1 on paper; use ink on pastel, and deep coral when a word needs colour.
- **Don't:** use red and green for good and bad; use a muted hairline card for "before" and an ink-outlined card with a butter highlight for "after", because a "bad" red would sit next to the coral signature and colour alone fails colour-blind readers.
- **Don't:** use LinkedIn blue #0A66C2 or indigo, because they blend with LinkedIn's interface and read as generic AI.
- **Dark slides:** none on LinkedIn; revisit for a website or talks.
- **Contrast checked with `color_check.py`:** ink on paper 16.6:1, ink on white 17.9:1, ink on coral 10.4:1, ink on butter 14.3:1, ink on lilac 11.6:1, muted on paper 5.6:1, deep coral on paper 4.6:1 (large text only), paper on ink 16.6:1.

### Typography

One family, **Onest** (Google Fonts, SIL Open Font License, free for commercial use, weights 100–900, wide language coverage), at two weights: 400 and 900. No monospace; numbers are set in Onest.

| Style | Size / weight | Line height | Letter-spacing | Use |
|---|---|---|---|---|
| Poster headline | 136 / 900 | 1.05 | -1.5% | Covers and section slides |
| Headline | 110 / 900 | 1.05 | -1.5% | Content slide headline |
| Subhead | 68 / 900 | 1.05 | -1.5% | Card titles, secondary headings |
| Step numeral | 200 / 900, deep coral | 0.85 | -1.5% | Leads step slides |
| Stat | 110 / 900 | 1.0 | -1.5% | The one number on a stat slide |
| Body | 42 / 400 | 1.45 | 0 | Paragraphs, card text |
| Label | 32 / 400, muted | 1.45 | 0 | Context above a headline, chart labels |
| Name line | 32, name 900 / role 400 | 1.3 | 0 | Author block |

- **Do:** keep everything at 32px or larger, because smaller text is unreadable at phone size.
- **Do:** use 900 for headlines, stats and names, and 400 for everything else, because two weights give maximum contrast with no guesswork.
- **Do:** write in sentence case with no full stops on headlines, because it reads like a person talking.
- **Don't:** let body run past three lines on a slide, because each slide carries one idea.
- **Don't:** add a third weight for emphasis; use deep coral or the butter highlight.

### Space and layout

- **Density:** airy. Poster type needs room, and space signals confidence.
- **Base unit:** 8px. Spacing scale: 8, 16, 24, 32, 48, 64, 96, 128.
- **Slide grid:** 1080 x 1350, 96px margins on all sides, 6 columns with 32px gutters (content width 888px).
- **Layout character:** left-aligned and top-anchored, never centred, because the category is full of centred hero layouts and left alignment reads faster on a phone.
- **Cover layout** (from the one-pager header): circular headshot top right, poster headline below it, left-aligned; name line at the bottom left.
- **Content footer:** small headshot, name and progress ("2 / 6") along the bottom margin, so the author stays visible and readers know how far through they are.
- **Breakpoints:** not needed for LinkedIn images; define when a website is built.

### Shape and elevation

- **Radius:** 0 for slides (LinkedIn crops images square-cornered), 24 for cards and photos, 12 for checkboxes and small elements, pill (999) for tags and the CTA chip.
- **Borders:** hairline 2px #E6DFCF for everyday cards; key outline 4px ink #1A1712 for the one idea per slide (about 1.5px when viewed on a phone).
- **Elevation:** none. Depth comes from surface colour and outlines, never shadows, following Elementor's flat approach and keeping charts crisp.
- **Texture:** the graph-paper grid (see section 8). No noise, grain or gradients.

## 5. Components

LinkedIn carousels are static, so components are slide templates and the parts they share. Hover and focus states apply only when the system reaches a website.

- **Cover:** pastel background (coral by default), 120px circular headshot top right on a coral-200 or butter-200 tile offset behind it, poster headline, name line bottom left. One cover per carousel.
- **Step slide:** paper page with grid, deep coral numeral, headline, up to three lines of body, content footer.
- **Stat slide:** white page with grid, label, one mini chart, the stat at 110/900, one line of context.
- **Before and after slide:** paper page, label, a hairline card for "before" (muted text) and an ink-outlined card for "after" with butter on the winning phrase.
- **Checklist slide** (from the one-pager's "fix this first" column): paper page, headline, three items with 48px square checkboxes (4px ink outline, 12px radius); never more than three items.
- **Quote or insight slide:** butter or lilac background, poster headline only, name line. Use one per carousel at most.
- **End slide (CTA):** coral background, headline asking one specific thing, ink pill chip with paper text (for example "Follow for one AI workflow a week"), large headshot. One ask only.
- **Card:** #FFFAEE, 2px hairline, 24 radius, 40px padding; key variant with 4px ink outline. One key card per slide.
- **Tag:** paper-100 #F2EADB pill, 32px label text, 8 x 24 padding. Used sparingly, never as an uppercase eyebrow.
- **Highlight:** butter behind the phrase, 0.12em side padding, no rounded ends.
- **Author block:** headshot circle, name 900, role 400, both 32px.
- **Profile banner (1584 x 396):** coral background, one poster-weight line about what you build, grid on the right two thirds; keep the bottom left clear, because LinkedIn overlays the profile photo there.
- **Not needed now:** forms, navigation menus, alerts, modals. Define them when a website exists.

## 6. Motion and interaction

- **Character:** none on LinkedIn; carousels and posts are static images, and stillness suits "excited, not hyped".
- **For future web and video:** durations 120ms (state changes) and 240ms (entrances); one easing curve, cubic-bezier(0.2, 0, 0, 1). Elements move only to show a change of state, never to decorate.
- **Never moves:** headlines, charts' data and the author block.
- **Reduced motion:** honour the reader's setting by removing all transitions.

## 7. Imagery and voice

- **Headshot:** a real, recent photo with natural light and a plain background, cut into a circle, with a coral or butter tile offset behind it (from the pink tile in the Elementor inspiration). The same photo on every piece, because recognition builds on repetition.
- **Photography:** only real artefacts from your own work (screens, files, notes, the workflow you actually ran), placed inside a card with a 24 radius. No stock photography and no AI-generated people or scenes, because principle 1 says built, not imagined.
- **Screenshots:** cropped tight to the part that matters, shown in a hairline card on a white data slide, with the key part marked by a butter highlight or ink outline.
- **Illustration:** none beyond the infographic kit; no robots, brains, sparkles or glowing orbs.
- **Icons:** Phosphor Icons, Bold weight (MIT licence, free), in ink, at 64px or larger. Bold matches the 900 headlines; used only where an icon carries meaning. This resembles the common stock-icon default, so keep icons rare and never decorative.
- **Graphic devices:** the graph-paper grid, the butter highlighter, deep coral step numerals, ink outlines and the coral tile behind the headshot. Nothing else.
- **Voice:** write as yourself, warm, specific and concrete, explaining through a real example. Energy comes from the result and the number, not from adjectives.
- **Words to avoid:** game-changer, unlock, supercharge, seamless, revolutionise, delve, "let's dive in", "it's not just X, it's Y", emoji bullets, all caps, em dashes.
- **Copy patterns:**
  - Hook: a specific outcome with a number ("I gave Claude my worst Monday and got three hours back").
  - Step headline: an imperative with a concrete object ("Give it the context you'd give a teammate").
  - Stat label: what was measured, in plain words ("Where the Monday went").
  - End slide: one specific ask, never "Like and share".

## 8. Additional layers

### Infographic language (from the one-pager inspiration)

A small, reusable kit of mini charts, each making one point.

- **Bar:** 3 to 5 bars, one coral, the rest paper grey #D7D0C1, 10px top radius, no axis lines except a 3px baseline; direct labels at 32px.
- **Dot grid (waffle):** 10 columns, coral dots for the share that matters, grey for the rest; label the count directly.
- **Line:** a 6px grey line with a coral dot on the point that matters and a 32px label beside it; no gridlines beyond the graph paper.
- **Step bars with people icons** (from the one-pager): grey steps growing left to right, the last in coral, with Phosphor person icons above.
- **Checklist:** see the checklist slide.
- **Icon group:** two to four Phosphor icons in a row with 32px labels, for a process or set of tools.
- **Rules:** one chart per slide; label data directly rather than with legends; no 3D, no gradients, no pie charts (hard to compare at phone size); the coral element must be the point of the slide's headline.

### Graph-paper grid (from the one-pager inspiration)

- 54px square cells (20 x 25 on a slide), 3px lines in #E3DACA, starting at the slide edge. Lighter lines disappear at phone size.
- Used on paper content slides and white data slides, and behind the right two thirds of the profile banner. Never on covers or quote slides, so they stay bold in the feed.
- Content never aligns to the grid lines on purpose; the grid is texture that says "worked out", not a layout grid.

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
| C7 | Semantic roles | Page: paper #FAF6EC by default; white #FFFFFF page variant for data-heavy or infographic slides (cards switch to paper #FAF6EC). Cards: #FFFAEE with hairline #E6DFCF for everyday content; ink-outlined (4px #1A1712 on a 1080px slide, about 1.5px on a phone) for the single key takeaway, checklist or fix. Text: ink #1A1712, muted #6B6152, deep coral #BC4C31 for emphasis, butter #FFE58F highlight | bespoke | Combination of options 2, 3 and 5; ink outline from Elementor's black and white edge | 3 One idea, one glance (the ink outline always marks the one idea) | Wanted both page colours and both card styles, with clear jobs | 2026-10-24 |
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
| T9 | Typographic details | Sentence case everywhere; headlines without full stops; body never longer than three lines on a slide | bespoke | Principle 3 | 3 One idea, one glance | Picked option 2 after seeing them rendered | 2026-10-24 |
| S1 | Density | Airy: generous margins and space around poster type | bespoke | Poster scale (T5) needs room | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| S2 | Base unit and spacing scale | 8px base; 8, 16, 24, 32, 48, 64, 96, 128 | bespoke | Standard 8px rhythm, scaled for 1080px slides | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| S3 | Grid | 1080 x 1350 slide, 96px margins, 6 columns, 32px gutters, 888px content width | bespoke | LinkedIn 4:5 carousel format | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| S4 | Breakpoints | Not needed for LinkedIn images; define with a website | bespoke | Medium research | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| S5 | Layout character | Left-aligned and top-anchored, never centred. Cover: headshot circle top right, poster headline below, name bottom left. Content footer: small headshot, name, progress "2 / 6" | bespoke | One-pager header; breaks the centred-hero convention | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| E1 | Radius scale | 0 slides, 12 small elements, 24 cards and photos, pill for tags and CTA chip | bespoke | Elementor's rounded cards and pill badges, scaled to slides | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| E2 | Borders | Hairline 2px #E6DFCF; key outline 4px ink #1A1712 | bespoke | C7 card styles at slide scale | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| E3 | Elevation | None: depth from surface colour and outlines, no shadows | bespoke | Elementor's flat, no-shadow approach | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| E4 | Texture | Graph-paper grid only; no noise, grain or gradients | bespoke | Accepted grid layer | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K1 | Component character | Flat, outlined, slide templates rather than UI controls | bespoke | LinkedIn carousels are static | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K2 | Buttons and links | End-slide CTA chip: ink pill, paper text, one ask | bespoke | Elementor's solid black buttons | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K3 | Form inputs | Not needed | bespoke | No forms on LinkedIn | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K4 | Cards and containers | #FFFAEE, 2px hairline, 24 radius, 40px padding; key variant 4px ink outline | bespoke | C7 | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K5 | Navigation | Content footer with headshot, name and "2 / 6" progress | bespoke | Encourages swiping; principle 4 | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K6 | Feedback | Not needed | bespoke | No system states on LinkedIn | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K7 | Data display | Infographic kit (section 8), checklist with 48px square checkboxes, paper tags | bespoke | One-pager charts and checklists | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K8 | Overlays | Not needed | bespoke | No overlays on LinkedIn | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| K9 | Product-specific components | Cover, step, stat, before and after, checklist, quote, end slide, author block, profile banner 1584 x 396 | bespoke | Brief: carousels, posts, banner | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| M1 | Motion character | None on LinkedIn (static images) | bespoke | Principle 5 | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| M2 | Durations | 120ms state changes, 240ms entrances (future web and video) | bespoke | Common, calm values | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| M3 | Easing | cubic-bezier(0.2, 0, 0, 1), one curve for everything | bespoke | Decelerating, unfussy | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| M4 | State changes | Web only: ink outline appears on focus; no hover lifts | bespoke | Flat system, no shadows | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| M5 | What moves | Only elements showing a change of state; headlines, data and author never move | bespoke | Principle 3 | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| M6 | Reduced motion | Remove all transitions when the reader asks for reduced motion | bespoke | Accessibility | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| I1 | Photography | Real headshot in a circle with an offset coral or butter tile; real artefacts from own work in cards; no stock or AI-generated scenes | bespoke | Elementor's photo-plus-pink-tile treatment; principle 1 | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| I2 | Illustration | None beyond the infographic kit; no robots, brains, sparkles | bespoke | Principle 1; breaks category conventions | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| I3 | Iconography | Phosphor Icons, Bold weight (MIT), ink, 64px+, rare and meaningful (resembles stock-icon default; kept deliberate) | bespoke | Matches the 900 headlines | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| I4 | Graphic devices | Graph-paper grid, butter highlighter, deep coral numerals, ink outlines, coral tile behind headshot | bespoke | Earlier decisions and accepted layers | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| I5 | Voice | The author's own voice: warm, specific, concrete examples; energy from results, not adjectives; words-to-avoid list | bespoke | Principle 5 | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| I6 | Copy patterns | Hook with a specific outcome and number; imperative step headlines; plain stat labels; one specific ask on the end slide | bespoke | Test copy in the brief | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| L1 | Infographic language | Bar, dot grid, line, step bars with people icons, checklist, icon group; one chart per slide, direct labels, coral marks the point, no pie charts or 3D | bespoke | Accepted layer from the one-pager | Delegated to the skill; serves the principles | delegated | 2026-10-24 |
| L2 | Graph-paper grid | 54px cells, 3px #E3DACA lines, on paper and white content slides and the right of the banner; never covers or quote slides | bespoke | Accepted layer from the one-pager | Delegated to the skill; serves the principles | delegated | 2026-10-24 |

## 11. Not yet decided
- Dark mode (C9): revisit for a website or talks.
- Breakpoints, forms, navigation menus, alerts and overlays: define when a website exists.
- Every "delegated" decision in the log can be revisited.

## 12. Inspirations and changelog
| Date | Change | Inspiration | Decisions affected |
|---|---|---|---|
| 2026-10-24 | System created (colour and type chosen by the user; remaining layers delegated) | Elementor website and screenshots; one-pager infographic | All |
