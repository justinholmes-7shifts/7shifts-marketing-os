# 7shifts Brand Guidelines

Source of truth for how anything we ship should look and sound. Distilled from the Winter 2024 brand system (Fuzzco). Full source: `assets/Brand Guidelines-compressed.pdf` (162pp) and `assets/7shifts Powerpoint slide templates.pdf` (146pp). Asset library: `assets/Logos/`, `assets/Fonts/`.

> When producing any visual artifact (readout, slide, page, social), pull styling from this file. Don't invent colors, fonts, or layout defaults.

---

## The brand in one breath

- **Tagline:** Great teams make great restaurants.
- **Guiding idea:** On your side, by your side.
- **Vision:** Elevating the standard of what restaurant teams can achieve together.
- **Hero of every story:** the operator and the staff — never 7shifts. We're the trustworthy sidekick.
- **Three pillars:** (1) Simple experiences, powerful technology · (2) For restaurants, today and always · (3) Teams at the heart of successful restaurants.

**Three things to remember:** On your side, by your side. → Simple, but powerful (restraint is the brand). → Great teams make great restaurants (the operator is the hero).

---

## Color

### Primary palette
| Name | Hex | RGB |
|---|---|---|
| **Curacao** (blue) | `#4370FF` | 67, 112, 255 |
| **Mojito** (green) | `#02FEB3` | 2, 254, 179 |
| **Empress** (purple) | `#C293F1` | 194, 147, 241 |
| **Chef's Coat** (white) | `#FFFFFF` | 255, 255, 255 |
| **Marshmallow** (off-white) | `#F1F0EC` | 241, 240, 236 |
| **Caviar** (black) | `#000000` | 0, 0, 0 |

### Secondary — tints (light)
| Name | Hex |
|---|---|
| **Ice** (light blue) | `#D6E0FF` |
| **Zest** (light green) | `#C6FF94` |
| **Lavender** (light purple) | `#EBDCFF` |

### Secondary — shadows (deep)
| Name | Hex |
|---|---|
| **Ranch** (deep blue) | `#193F78` |
| **Pesto** (deep green) | `#244F47` |
| **Baba Ganoush** (deep purple) | `#453E75` |

### Neutrals
| Name | Hex | Role |
|---|---|---|
| **Marshmallow** | `#F1F0EC` | Light backgrounds |
| **Oat** | `#E3D9D2` | Slightly warmer light bg |
| **Earl** | `#6E6D6C` | Body text, secondary text |

### Legacy accent — use sparingly
| Name | Hex | Role |
|---|---|---|
| **Spritz** (orange) | `#FF6709` | Accent only: two-color logo, data viz, illustration accents. **Never** a flood background or text on black. ~6% of any composition. |

### Composition recipe (every layout / bento)
1. **One** dominant primary color (a second primary may appear, but one dominates).
2. **1–2** secondary colors (tints or shadows) for support.
3. **Anchor** with a light neutral or black (or both).
4. Spritz **only** through logo, data viz, or illustration accents.
5. Photography can be used throughout.

**Rough distribution:** primaries & tints ~36% · light neutrals ~30% · Caviar ~13.5% · shadows ~7.5% · Spritz ~6%.

### Do NOT
- Spritz as a flood background or text on black.
- Color on color (e.g. Curacao text on Mojito).
- Illustrations in any color other than black (+ optional Spritz or white accent).

### Verified accessible pairings
Curacao + white (AA large) · Caviar + Mojito (AAA 17:1) · Caviar + Empress (AAA 10:1) · Caviar + Ice/Zest/Lavender (AAA 16–18:1) · White + Ranch/Pesto/Baba Ganoush (AAA 11–13:1) · Earl on Marshmallow (AAA 15:1).
**Rule of thumb:** black text on a tint, white text on a shadow.

---

## Typography

Two typefaces, no exceptions. Files in `assets/Fonts/`.

- **Universal Sans** (custom 7shifts cut) — display. Headlines, large display, small CTAs/buttons. Default weight Regular 500. **Always −2 letter kerning on headlines.**
- **SF Pro Text** — body & utility. Body copy, eyebrows, longer reading. Medium for body, Bold for emphasis.

| Element | Typeface | Notes |
|---|---|---|
| Eyebrow | SF Pro Text | Small, above headline |
| Heading | Universal Sans | −2 kerning, tight tracking + line-height |
| Body | SF Pro Text | Tight but breathing |
| Small + CTAs | Universal Sans | e.g. "Let's Go!" |

**Headline shape:** balanced block (hourglass / hill / crescendo). Avoid ragged right edges, single-word last lines (widows), narrow lumpy lines. **Line length 6–8 words.**

**Web fallback:** Universal Sans isn't web-standard — fall back to `system-ui, -apple-system, Inter, sans-serif` for previews and note it in handoff.

---

## Logo

Two **independent** components — never locked together (the symbol's "7" repeats the wordmark's "7"). Files in `assets/Logos/` (Icon + Wordmark, in SVG/PDF/PNG).

- **Symbol** — orange stopwatch "7" in a circle, 45° angle, 1:1. Use when space is tight, or for social/app/avatars/favicons.
- **Wordmark** — Swiss-inspired custom lettering.
  - On Curacao, black, or any shadow → wordmark **white**.
  - On any tint or light neutral → wordmark **black**.
  - **Never on Spritz.**

**Clear space:** wordmark = one "S"-height all sides; symbol = width of the stopwatch button.

**Never:** stretch/skew/rotate/outline, add shadows/effects, recolor the wordmark, image-fill the symbol, lock symbol + wordmark together, or alter either drawing.

---

## Voice & tone

**Voice (never changes):** Knowledgeable, Clear, Warm, Helpful. The operator and staff are the hero; 7shifts is the trustworthy sidekick.

➡️ **Verbal voice lives in [`voice.md`](voice.md)** — tone by audience, calibration, sanctioned statements, restaurant vocab, and what we never write. That's the single source for how we write. This file owns the visual system; `voice.md` owns the words.

---

## Audiences

- **Primary — Operators (buyers):** owners, GMs, directors of ops at restaurants (QSR/FSR/franchise, 16–75 employees/location). Got in because they love food, not to get rich. Juggling everything, worried about getting the numbers wrong, want **peace of mind**. Skeptical of point solutions that overpromise. Speak with empathy, confidence, concrete utility.
- **Secondary — Employees (users):** servers, hosts, kitchen crew, bartenders. Want predictability, schedule visibility, to feel valued. Speak like a friend who respects their time.

The competitive set: Excel, Toast, Square, Homebase, HotSchedules. 7shifts is the only one that is restaurant-specific, easy to use, and built in one app. Trusted by 50,000+ restaurants.

---

## Photography

**Feel:** gritty, high-contrast, flash photography, in-action, not posed.
**Subjects (priority):** (1) People — real, varied hospitality workers · (2) Product in use, in-context · (3) Interactions where people + product meet.
**Avoid:** stocky staged shots, glossy corporate, overlit smiles, generic-SaaS-website energy.

**AI photo base prompt:** "Raw 35mm flash photography, harsh on-camera flash lighting creating hard shadows and bright specular highlights, high contrast, gritty texture with visible film grain, chaotic and frantic atmosphere, motion blur indicating speed and energy, stainless steel reflections, sweaty and greasy surface textures, unposed and candid snapshot aesthetic, vivid color grading with deep crushed blacks and punchy saturation, lo-fi authentic mood, intense and visceral, low-light environment illuminated by a sudden burst of light."

---

## Illustrations & icons

**Style:** mono-linear, monochromatic, an ode to the restaurant space with human expression. Organic strokes (Blob Brush / smooth round brush), varied line thickness for depth, embrace imperfection.

**Color:** always **black** base. May add **one** solid-fill accent — Spritz on white/neutral backgrounds, white on colored backgrounds. Never both, never any other color, never all-white.

**Subject matter:** kitchen tools, dishes, hands, aprons, the line, the dish pit.

---

## The Bento system (layout language)

The organizing metaphor for 7shifts marketing surfaces: a contained grid where every compartment holds a discrete piece, all united in one place — modularity, order despite chaos. **This is how slides and the readout should be composed.**

**Every bento combines:** (1) a product feature module (simplified UI, one idea — not a full screenshot) · (2) a gritty in-action photo · (3) headline/text in Universal Sans on a colored background · (4) a mono-linear illustration.

**Construction rules:** 20px gutter between cells · generous corner rounding (match 7shifts UI radius) · each composition tells a small narrative (sequence, don't stack) · vary cell sizes (some big, some small) · wordmark or symbol can anchor one cell.

**Slides specifically:** treat each slide as a bento. One dominant primary, one supporting secondary, anchored in Marshmallow or Caviar. Universal Sans titles, SF Pro Text body. Never Spritz as a slide background.

---

## Restraint is the brand

If a layout feels busy, strip it back. If a headline reads like a feature list, rewrite it as an outcome. The system is intentionally restrained — reach for a stronger primary or a tint pairing before reaching for more color.
