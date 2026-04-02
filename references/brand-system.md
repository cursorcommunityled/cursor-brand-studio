# Cursor Brand System

Comprehensive brand reference for all Cursor content creation. Read this file on EVERY activation before producing any output.

## Color System

### Light Theme

- bg: #F7F7F4 — Main background
- fg: #26251E — Primary text (headings, titles, body)
- fg-secondary: #26251E at 60% opacity (~#66655E) — Subtitles, captions
- accent: #F54E00 — Links, CTAs, data highlights ONLY. Never headings or body text
- card: #F2F1ED — Card backgrounds
- card-01: #F0EFEB — Card level 1
- card-02: #EBEAE5 — Card level 2
- card-03: #E6E5E0 — Card level 3

### Dark Theme

- bg: #14120B — Main background (use #000000 for full-black slides)
- fg: #EDECEC — Primary text (headings, titles, body)
- fg-secondary: #EDECEC at 60% opacity (~#9E9D99) — Subtitles, captions
- accent: #F54E00 — Links, CTAs, data highlights ONLY
- card: #1B1913 — Card backgrounds (use #111111-#141412 for slides)
- card-border: #FFFFFF at 10-15% opacity — Subtle card borders

### Accent Color Rules

The accent orange #F54E00 is ONLY for: interactive elements (buttons, links), data callouts (stat numbers when emphasis needed), and small UI highlights. NEVER use accent for headings, body text, labels, or metadata. The accent is sparing and sharp, not prominent.

## Contextual Text Color — CRITICAL

Text color depends on the SPECIFIC BACKGROUND BEHIND THE TEXT, not the overall slide theme. Before placing ANY text, check the exact background region behind it.

- Light gray base (#F7F7F4 / #E8E8E4): use #26251E for primary, ~#66655E for secondary
- Dense gradient blob (saturated orange/magenta/purple): use #FFFFFF
- Sparse/transparent gradient on light base: use #26251E (the base shows through)
- Solid black (#000000): use #EDECEC for primary, ~#9E9D99 for secondary
- Dark card (#111111-#1B1913): use #EDECEC for titles, ~#9E9D99 for descriptions

If the background is a gradient, check the specific zone where the text lands — not the overall slide. Text that sits on a light corner of a gradient slide still gets dark text.

## Typography

### Typeface
Cursor Gothic — official brand typeface. Weights: Regular, Bold, Italic, Bold Italic.
Font files: assets/fonts/CursorGothic-{Regular,Bold,Italic,BoldItalic}.ttf

For PPTX: set fontFace to "Cursor Gothic". Falls back to system sans-serif if unavailable.

### Sizing (slides 16:9, 10 x 5.625 inches)

- Slide title (hero): 40-52pt Bold
- Section heading: 26-32pt Bold
- Card/block heading: 12-14pt Bold
- Body text: 11-13pt Regular
- Metadata/labels: 9-10pt Bold or Regular
- Stat numbers: 40-48pt Bold
- Stat labels: 9-10pt Regular

### Casing
Sentence case for ALL headings, labels, titles. No title case except proper nouns.

YES: "Improved agent tools, steerability, and usage visibility"
NO: "Improved Agent Tools, Steerability, and Usage Visibility"

## Voice and Tone

Quiet confidence: clear, concise, approachable. Technical when needed, light when possible. Professional, sometimes witty, never forced.

- Say things simply and directly
- Be clear and concise, but complete
- Stay professional and considerate
- Do NOT oversell or exaggerate
- Do NOT try too hard to be funny or casual
- Do NOT hide meaning in jargon or corporate speak

## Logo Usage

### Variants Available (in assets/logos/)
- Horizontal lockup: LOCKUP_HORIZONTAL_2D_DARK.png / LIGHT.png
- Vertical lockup: LOCKUP_VERTICAL_2D_DARK.png / LIGHT.png
- Cube only: CUBE_2D_DARK.png / LIGHT.png, CUBE_25D.png (metallic 2.5D)
- Wordmark: WORDMARK_DARK.png / LIGHT.png

### Logo Rules
- Use provided lockups only — never create custom ones
- Min clear space around cube: 1/3 cube width
- Primarily use the 2D version
- Use with restraint — never oversized
- CUBE_25D for special emphasis (section dividers, hero slides)

### Selection by Background
- Light/gray: use LIGHT variant (dark logo on light bg)
- Black/dark: use DARK variant (white logo on dark bg)
- Dense gradient: use DARK variant (white logo)
- Sparse gradient on light base: use LIGHT variant (dark logo)

## Spacing (slides)

### Margins
- Slide edge to content: min 0.6", prefer 0.7"
- Top header bar: y = 0.4" from top

### Vertical Rhythm
- Header to main title: min 1.0" gap
- Title to subtitle: min 0.3" (prefer 0.4-0.5")
- Between content sections: min 0.5"
- Stat number to label: 0.15-0.2"
- Card internal padding: 0.2-0.25"

### Horizontal
- Two-column: left ~40%, right ~50%, ~10% gap
- Card grids: 0.2-0.25" gap between cards
- Stats row: evenly distributed across slide width

## Gradient System

Signature gradient: warm-to-cool radial blobs (orange, yellow, magenta, purple, blue). NOT linear gradients.

### Pre-Rendered Backgrounds
Gradient backgrounds are pre-rendered 1920x1080 PNGs in assets/backgrounds/. Always use these as slide background images. Never attempt to recreate gradients programmatically — python-pptx and PptxGenJS cannot produce multi-color radial blur effects.

See references/slide-light-patterns.md and references/slide-dark-patterns.md for the background catalog with layout specs.
