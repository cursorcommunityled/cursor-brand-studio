# Dark Theme Slide Patterns

Layout specifications for the dark (enterprise/community) theme. Read this when creating dark-themed presentations.

## Background Catalog

### bg_dark_solid.png (or just color #000000)
Use for: Title slides, stats slides, testimonials, card grids. The most common dark background — pure black with no decoration.

### bg_dark_gradient.png
Use for: Two-column layouts where the left side has visual impact. Visual: left ~40% has warm gradient blur (same orange/magenta/purple palette as light theme), right ~60% is solid dark. Content goes on the dark right side.

## Layout: D1 — Dark Title Slide

Background: solid #000000

### Structure
- Logo centered horizontally
- Tagline below logo, centered
- Optional stats row in lower half

### Specs (title only)
- Logo: LOCKUP_HORIZONTAL_2D_DARK, centered x:3.4 y:0.7 w:3.2 h:0.76
- Tagline: centered, fontSize 26, color #9E9D99 (secondary)

### Specs (with stats)
- Logo: same as above
- Tagline: x:1.5 y:2.0 w:7, fontSize 26, centered, color #9E9D99
- Stats row y: 3.3
- Stat numbers: fontSize 42, bold, color #EDECEC, centered in 2.8" wide columns
- Stat labels: fontSize 10, color #9E9D99, centered below (y offset +0.75")
- Column positions (3 stats): x:0.5, x:3.45, x:6.4, each w:2.8

### Rules
- Stats should not overlap — if "100,000" is too wide at 42pt, reduce to 38pt
- Verify text width before placing: at ~9px per character at 42pt bold, "100,000" needs ~63px per char = ~4.4" — ensure column is wide enough

## Layout: D2 — Dark Card Grid

Background: solid #000000

### Structure
- Title + subtitle at top
- 2x3 or 2x2 card grid below

### Specs
- Title: x:0.7 y:0.5 w:8, fontSize 28, bold, color #EDECEC
- Subtitle: x:0.7 y:1.15 w:8, fontSize 11, color #9E9D99
- Card grid starts: y:1.75
- Card size: w:2.7 h:1.55 with 0.25" gaps
- Card fill: #141412
- Card border: #2A2A28, width 0.5pt
- Card corner radius: 0.1"
- Card title: internal x+0.25 y+0.25, fontSize 12, bold, color #EDECEC
- Card description: internal x+0.25 y+0.9, fontSize 9, color #9E9D99

### Rules
- Cards arranged in rows of 3
- Last row may have fewer cards — left-aligned, not centered
- Card descriptions should be 1-2 sentences max
- If a card has an icon, place it at top of card (y+0.15) as a small image (0.35x0.35")

## Layout: D3 — Dark Testimonials

Background: solid #000000

### Structure
- Section title at top
- 2-3 testimonial cards in a row

### Specs
- Title: x:0.7 y:0.7, fontSize 28, bold, color #EDECEC
- Cards start: y:2.0
- Card size: w:2.9 h:2.8 with 0.15" gaps
- Card fill: #141412, border: #2A2A28
- Quote mark: fontSize 24, color #9E9D99, positioned at top-left of card
- Quote text: fontSize 11, color #EDECEC, below quote mark
- Attribution: fontSize 9, bold, color #9E9D99, near bottom of card
- Company logo: small image at bottom-right of card

## Layout: D4 — Gradient Split

Background: bg_dark_gradient.png

### Structure
- Left column (on gradient): large heading text, white
- Right column (on dark): content blocks with bullet points

### Specs
- Left heading: x:0.7 y:1.5 w:3.5, fontSize 30, bold, color #FFFFFF
- Right content: x:5.0 y:0.5 w:4.5
- Content blocks: heading (14pt bold #EDECEC) + bullets (11pt #9E9D99)

### Rules
- Text on the gradient side MUST be white
- Text on the dark side uses standard dark theme colors
- Do not place secondary/muted text on the gradient — only bold white headings

## General Dark Theme Rules

1. Never use gray text (#9E9D99) on the gradient portions — only on solid dark backgrounds
2. Card borders should be barely visible — just enough to define the card edge
3. Logo company images in testimonials should be the white/light variant
4. Stat numbers are the brightest elements — they should pop as #EDECEC or #FFFFFF
5. Maintain at least 0.5" between the last content element and the slide bottom edge
