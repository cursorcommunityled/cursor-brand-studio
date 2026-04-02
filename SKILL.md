---
name: cursor-brand-studio
description: Cursor brand content studio for ambassadors and community. Use when creating presentations, slides, decks, social media posts, landing pages, banners, images, one-pagers, or any content following Cursor brand guidelines. Triggers on "Cursor slides", "Cursor presentation", "Cursor deck", "Cursor post", "Cursor landing page", "Cursor banner", "Cursor brand", "brand guidelines", "ambassador content". Reads brand-system.md on every activation. Reads slide pattern files only for presentation tasks. Do NOT use for general slide creation unrelated to Cursor brand or for Cursor IDE technical support.
license: CC-BY-4.0
metadata:
  author: Felipe Rodrigues - github.com/felipfr
  version: 1.0.0
---

# Cursor Brand Studio

Create brand-compliant content for the Cursor community — presentations, social posts, landing pages, documents, and more. Every output follows the official Cursor brand guidelines with pixel-level precision.

## First Step — Always

Before producing ANY output, read `references/brand-system.md`. It contains the complete color system, typography rules, voice guidelines, logo usage rules, and the critical contextual text color rules. Do not skip this step.

## Content Type Detection

Determine which type of content the user is requesting:

1. **Presentation/Slides** — keywords: slides, deck, presentation, pptx, workshop, meetup, talk
2. **Social media post** — keywords: post, LinkedIn, Twitter/X, social, announcement
3. **Landing page** — keywords: landing page, event page, website, HTML
4. **Banner/image** — keywords: banner, image, graphic, cover image, thumbnail
5. **Written document** — keywords: one-pager, guide, document, brief, memo

Then follow the instructions for that content type below.

## Content Type: Presentations (PPTX)

This is the primary use case. Read the relevant pattern files before starting:
- `references/slide-light-patterns.md` — for light/workshop/community theme
- `references/slide-dark-patterns.md` — for dark/enterprise theme
- Read BOTH if user wants mixed or does not specify

### Theme Selection

Ask the user which theme unless context makes it obvious:
- **Light theme** (workshop style): warm gray background, gradient blobs, black text. Best for community workshops, meetups, tutorials.
- **Dark theme** (enterprise style): black background, white text, subtle cards. Best for enterprise pitches, corporate talks.
- **Mixed**: dark for title/closing, light for content (common pattern).

### Slide Generation Workflow

1. **Plan the deck**: Propose a slide outline (title, content slides, section dividers, closing). Get user approval before generating.

2. **Select backgrounds**: For each slide, pick the appropriate pre-rendered background PNG from `assets/backgrounds/`. Match slide purpose to layout pattern.

3. **Generate PPTX using PptxGenJS**: Use the pptx skill for setup and best practices. Critical settings:
   - `pres.layout = "LAYOUT_16x9"` (always 16:9)
   - `fontFace: "Cursor Gothic"` for all text
   - Background via `slide.background = { data: img64("path/to/bg.png") }`
   - Colors: 6-char hex WITHOUT # prefix (PptxGenJS requirement)
   - Never use 8-char hex for transparency — use `transparency` property instead

4. **Apply layout specs**: Follow exact coordinates from pattern files. Do not improvise positions.

5. **Verify text colors**: For EVERY text element, check which background region it sits on and apply the correct color from the contextual color rules in brand-system.md. This is the most common error source.

6. **QA**: Convert to PDF then images, visually inspect every slide. Check for: text overflow, overlapping elements, wrong colors, spacing violations, logo placement.

### Background Assets (in assets/backgrounds/)

- `bg_light_title.png` — Light theme title: gradient blob right on gray base
- `bg_light_content.png` — Light theme content: sidebar strip + small blob, clean gray
- `bg_light_fullgradient.png` — Full vibrant gradient: section dividers, impact slides
- `bg_dark_solid.png` — Pure black (or use `{ color: "000000" }`)
- `bg_dark_gradient.png` — Dark with gradient blur on left ~40%

### Logo Assets (in assets/logos/)

PNG versions pre-converted from SVG: LOCKUP_HORIZONTAL_2D_DARK.png, LOCKUP_HORIZONTAL_2D_LIGHT.png, CUBE_25D.png, and all other variants listed in brand-system.md.

### Font Assets (in assets/fonts/)

CursorGothic-Regular.ttf, CursorGothic-Bold.ttf, CursorGothic-Italic.ttf, CursorGothic-BoldItalic.ttf

### Common Slide Mistakes to Avoid

1. Using accent orange (#F54E00) for heading text — accent is ONLY for CTAs and data highlights
2. Using muted gray text on gradient backgrounds — use white on dense gradients
3. Placing text on the dense gradient zone of bg_light_title — keep text on the clear gray left side
4. Forgetting sentence case — all headings are sentence case
5. Cramped spacing — follow minimum spacing from brand-system.md
6. Oversizing the logo — use modest sizes with breathing room
7. Not checking the specific background region behind each text element

## Content Type: Social Media Posts

### Text Format
Follow Cursor voice: clear, concise, confident. No hype, no excessive emojis, no buzzwords.

Structure: Hook (first line) → Body (2-4 sentences) → CTA → Hashtags (2-3 max, minimal)

### Accompanying Images
If user wants a visual: create as HTML or SVG using brand colors. Dark theme preferred for social (more impact). Include cube logo small in corner. Sizes: 1200x628 for LinkedIn, 1200x675 for Twitter/X, 1080x1080 for square.

## Content Type: Landing Pages (HTML)

Generate single HTML file with inline CSS. Use brand color system as CSS custom properties:

Light: --cursor-bg: #F7F7F4, --cursor-fg: #26251E, --cursor-accent: #F54E00
Dark: --cursor-bg: #14120B, --cursor-fg: #EDECEC, --cursor-accent: #F54E00

Use `@media (prefers-color-scheme: dark)` for automatic theme switching. Font: "Cursor Gothic" with system sans-serif fallback. Max width 1200px, generous padding (80px+ vertical sections).

## Content Type: Banners/Images

Generate as SVG or HTML. Apply brand colors and Cursor Gothic. Include cube logo subtly. Common sizes: LinkedIn banner 1584x396, Twitter header 1500x500, event banner 1920x1080, square social 1080x1080.

## Content Type: Written Documents

Generate as Markdown or DOCX. Apply Cursor voice throughout. Sentence case for headings. Clear concise language. Short paragraphs (3-5 sentences). Prefer prose over bullet lists.

## Examples

### Example 1: Workshop Presentation

User says: "Create a Cursor intro workshop presentation with 10 slides"

Actions:
1. Read brand-system.md, slide-light-patterns.md
2. Propose outline: title, agenda, "What is Cursor?", 4 feature slides, live demo divider, best practices, Q&A, closing
3. Generate PPTX with bg_light_title for slide 1, bg_light_content for content, bg_light_fullgradient for dividers
4. Apply L1 layout for title, L2 for content, L4 for dividers
5. QA all slides visually

Result: 10-slide PPTX ready for Google Slides import, brand-compliant.

### Example 2: Enterprise Pitch

User says: "Create a Cursor enterprise pitch, dark theme"

Actions:
1. Read brand-system.md, slide-dark-patterns.md
2. Propose enterprise-focused outline
3. Generate PPTX with solid black backgrounds, dark card layouts
4. Apply D1 for title, D2 for cards, D3 for testimonials
5. QA all slides

Result: Professional dark PPTX with stats, cards, testimonials.

### Example 3: LinkedIn Post

User says: "Write a LinkedIn post announcing a Cursor meetup"

Actions:
1. Read brand-system.md voice section
2. Draft in Cursor voice: direct, clear, no hype
3. Suggest image specs if requested

Result: Ready-to-post text following brand voice.

## Troubleshooting

### Font not rendering in Google Slides
Cursor Gothic is not in Google Fonts. Users must install it locally or accept fallback font. Include this note when delivering presentations.

### Gradient mismatch with originals
Pre-rendered gradients approximate the originals. For pixel-perfect matching, export the original gradient from its source tool (Canva, Google Slides) and replace the background PNG.

### Text overlap on slides
Font metric differences between Cursor Gothic and fallback fonts cause different wrapping. Use conservative text widths (leave 20% extra room) and always run QA.
