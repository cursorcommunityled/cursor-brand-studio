# Light Theme Slide Patterns

Layout specifications for the light (workshop/community) theme. Read this when creating light-themed presentations.

## Background Catalog

### bg_light_title.png
Use for: Cover slides, section dividers, closing slides.
Visual: Large vibrant gradient blob (orange/yellow/magenta/purple) positioned center-right on warm light gray (#E8E8E4) base. The left ~45% of the slide is mostly clear gray — place text there.

### bg_light_content.png
Use for: All content slides (the workhorse layout).
Visual: Thin vertical gradient strip (5px, magenta-to-orange) on left edge with soft glow. Small gradient blob bottom-left. Rest is clean warm gray. Text goes everywhere except bottom-left corner.

### bg_light_fullgradient.png
Use for: High-impact section dividers, "What is Cursor?" style slides, closing/thank you slides.
Visual: Full-bleed vibrant gradient covering entire slide (orange top-left, magenta center, purple right, blue bottom-right). ALL text on this background MUST be white #FFFFFF.

## Layout: L1 — Title Slide

Background: bg_light_title.png

### Structure
- Header bar (y: 0.4"): Logo left (0.7"), date center, type right
- Main title (y: 1.6"): Large bold text, left-aligned, max 5.2" wide
- Subtitle (y: 3.5"): Smaller text below title, ~4.5" wide
- Community/speaker (bottom-right, y: 4.2"): Name + speaker info

### Specs
- Logo: LOCKUP_HORIZONTAL_2D_LIGHT, x:0.7 y:0.4 w:1.6 h:0.38
- Date text: x:4.0 y:0.4, fontSize 9, bold, color #26251E
- Type label (right): x:7.2 y:0.4, fontSize 9, bold, color #26251E, align right
- Title: x:0.7 y:1.6 w:5.2, fontSize 48, bold, color #26251E
- Subtitle: x:0.7 y:3.5 w:4.5, fontSize 13, color #66655E
- Community name: x:6.5 y:4.2, fontSize 16, bold, color #26251E
- Speaker: x:6.5 y:4.6, fontSize 11, color #66655E

### Rules
- ALL text on this slide is dark (#26251E) because it sits on the light gray side, NOT on the gradient
- The gradient blob is decorative — no text should be placed on top of the dense gradient area
- If a title is long, reduce fontSize to 40-44pt rather than letting it overflow into the gradient zone

## Layout: L2 — Content Slide (Two Column)

Background: bg_light_content.png

### Structure
- Left column (~40%): Section heading, large bold
- Right column (~50%): Content blocks with heading + bullets each
- No header bar on content slides

### Specs
- Section heading: x:0.7 y:1.0 w:3.8, fontSize 28, bold, color #26251E
- Content column start: x:5.0, width 4.5"
- Each content block: heading (13pt bold #26251E) + bullets (11pt #66655E)
- Space between blocks: 1.6" total height per block (heading 0.35" + bullets 1.0" + gap 0.25")
- First block starts: y:0.55
- Bullet paraSpaceAfter: 6pt

### Rules
- Max 3 content blocks per slide
- If content needs more space, split into multiple slides
- Left heading should vertically center relative to the content blocks

## Layout: L3 — Stats Slide (Light)

Background: bg_light_title.png or bg_light_content.png

### Structure
- Main statement at top
- 2-3 large stat numbers in a row
- Small labels below each stat

### Specs
- Statement: x:0.7 y:0.8 w:8, fontSize 22, color #26251E
- Stats row y: 2.5
- Each stat: fontSize 44-48 bold, color #26251E, centered in equal-width column
- Stat labels: fontSize 10, color #66655E, centered below

## Layout: L4 — Full Gradient Section Divider

Background: bg_light_fullgradient.png

### Structure
- Centered content: optional cube icon, large title, subtitle(s)

### Specs
- Cube (if used): CUBE_25D, centered x:4.55 y:1.2 w:0.9 h:1.03
- Title: centered, fontSize 40, bold, color #FFFFFF
- Subtitle: centered, fontSize 15, color #FFFFFF
- Secondary text: centered, fontSize 13, color #F0E8E0

### Rules
- ALL text on full gradient MUST be white (#FFFFFF or very light)
- Never use dark text on the full gradient background
- Keep text minimal — this is a visual impact slide, not a content slide
- Max 2-3 text elements

## Layout: L5 — Split (Text + Image)

Background: bg_light_content.png

### Structure
- Left column: heading + body text + optional callout
- Right column: screenshot, code snippet, or image

### Specs
- Left text: x:0.7 y:0.8 w:4.0
- Heading: fontSize 28, bold, color #26251E
- Subtitle label: fontSize 11, bold, color #00BFA5 (teal accent for "For: Category" labels)
- Body: fontSize 12, color #66655E
- Image area: x:5.2 y:0.5 w:4.3 h:4.5, with subtle rounded corners

### Rules
- Images should have a subtle shadow or border to separate from background
- Code screenshots look best with dark theme screenshots on the light slide background
