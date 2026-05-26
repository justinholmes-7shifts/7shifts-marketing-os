# Brand Designer: Request Playbook

How to handle the common asks. All of these assume the visual system in the marketing OS `context/brand-guidelines.md` (color hex, type specs, logo rules, photo, illustration, bento) and the copy voice in `context/voice.md`. Pull specifics from those, don't reinvent them here.

## "Design a social post for X"
Ask: which channel (IG, X, LinkedIn, TikTok)? Which audience (operators or employees)? Then propose: dimensions, primary color, layout (single bento cell or carousel), photo vs illustration vs product module, headline in Universal Sans (-2 kerning), one CTA in Universal Sans. Spritz only as the symbol or one illustration accent, never a flood.

## "Make a web hero / landing page module"
Default to a Curacao or Marshmallow background. Headline in Universal Sans at -2 kerning, 6-8 words per line, max two lines. Eyebrow in SF Pro Text above, body in SF Pro Text below. CTA pair: filled pill button (Caviar fill, white text) + ghost text link with a → arrow. Pair with a product module illustration, a gritty photo, or a bento composition to its right.

## "Create a presentation / slide deck"
Treat each slide as a bento composition. One dominant primary, one supporting secondary, anchored in Marshmallow or Caviar. Universal Sans for titles, SF Pro Text for body. Never Spritz as a slide background.

## "Design swag / merch"
Wordmark in white on Caviar is the canonical hoodie/tee treatment. Embroidered symbol (black "7" + Spritz orange ring) on Marshmallow or Oat backgrounds for hats and bags. Avoid Spritz as a flood color on apparel.

## "Make a co-brand lockup with [partner]"
Both wordmarks at equal optical weight, separated by a single vertical pipe (`|`) or "×" mark in the partner's brand color or a neutral. Honor the 7shifts wordmark clear space (one "S"-height on all sides). Never compromise the 7shifts wordmark color rules to match a partner.

## "Write the copy for X"
Apply the voice (Knowledgeable, Clear, Warm, Helpful) and the right tone for the audience. Lead with the operator's outcome ("Save time," "Spend less on admin"), not a feature list. One restaurant idiom per piece (86, knives down, last call), not three. Run it against `context/voice.md`: banned words, and the value-prop standard in `context/positioning.md` (a value prop names a metric, not functionality).

## "Design an illustration of [restaurant scene]"
Mono-linear black strokes, organic line quality, varied weight for depth. One optional solid-fill accent: Spritz if the background is white or neutral, white if on a colored background. Never both. Restaurant-grounded subject matter: kitchen tools, dishes, hands, aprons, the line, the dish pit.

## Output
Your default output is a designed asset, not a written design brief. Render HTML or SVG mockups inline whenever possible. When you produce code, use the actual hex values from `context/brand-guidelines.md`. Universal Sans isn't web-standard, so fall back to `system-ui, -apple-system, Inter, sans-serif` in previews and note it in the handoff.
