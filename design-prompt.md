# CRITICAL RULES (read these first)

1. **CTA text**: "Descubre Nuestros Aromas" — EXACT text on ALL primary CTA buttons
2. **Desktop only**: Design for 1440px wide. Do NOT create a mobile version.
3. **Overlines required**: Every section MUST have an overline above the title
4. **No generic layouts**: Fragrances as editorial alternating rows (NOT card grids)
5. **Screenshot after each section**: STOP, take a screenshot, verify quality before moving on
6. **Real content only**: Use content from this prompt verbatim. No placeholder text.
7. **Logo handling**: Do NOT use G() to reproduce the logo. Use a placeholder rectangle with text "LOGO" in `#763b13`. The code phase will embed the real file.

# QUALITY STANDARDS (minimum bar)

- Hero section: minimum 800px tall, gradient overlay visible, dramatic headline (56px+)
- Typography scale: 3:1+ ratio between headlines and body text
- Section dividers: visible transitions between sections (not just stacked rectangles)
- Spacing: 100px+ vertical padding per section, 24px+ between elements
- Color contrast: WCAG AA compliant (4.5:1 body text, 3:1 large text)

# ANTI-PATTERNS FROM PREVIOUS FAILURES

- Flat dark backgrounds without gradient depth or atmospheric glow
- Plain text lists instead of editorial rows with dividers
- AI-generated logos instead of placeholder rectangles
- Typography with no scale contrast (everything same size)
- Broken/clipped section dividers
- Card grids for fragrance listings — use editorial alternating rows instead
- Missing overlines on sections

# INDUSTRY-SPECIFIC RULES (Artisanal Home Fragrance / Perfumería)

## Visual Style
- Clean product shots on solid or linen backgrounds. Lifestyle shots secondary.
- Black (#1A1A1A) + ivory (#FAF7F3) + brown (#763b13) + gold (#C4A882) for luxury positioning
- Grid-based product layout. Hero with atmospheric product photography.
- Elegant serif for headings (Bon Voyage), clean sans for body (Neuzeit Grotesk)

## UX Specs
- Type scale: H1 56-64px (weight 400, tracking 0.12em), H2 36-42px, H3 24-28px, body 16-18px, overline 11-12px uppercase tracking 0.15em
- Spacing: section padding Y 100-120px, section padding X max-w-1280px centered, element gap 24-32px, card gap 20-24px
- CTA style: Outlined thin 1px button OR filled #763b13, uppercase, 44-48px height, tracking 0.15em
- Nav: Sticky top, transparent on hero → solid #1A1A1A on scroll, logo centered, height 64px

## RD-Specific Notes
- WhatsApp is the #1 communication channel — floating button MANDATORY
- Prices in RD$ (Dominican Pesos)
- Gift wrapping service mention (common in DR market)
- Instagram is primary discovery channel — link must be prominent

## Trust Signals
- "100% Cera de Soya Natural" badge
- Real product photography (not stock)
- Owner photo for personal connection
- Payment methods mentioned (bank transfer BHD/Popular)

## Anti-Patterns
- No prices hidden behind clicks — all prices visible inline
- No generic stock photos — use only real product imagery
- No auto-playing carousels
- No cluttered hero — one headline, one subheadline, one CTA

---

## Design Specification

# Design Spec: Lisenza Studio Landing Page

## Overview
A bilingual (ES/EN) e-commerce landing page for Lisenza Studio, an artisanal home fragrance brand in Santo Domingo, Dominican Republic. The page drives online sales through a WhatsApp cart flow. Visual direction: "Maison Noire" — elevated luxury with high-contrast editorial sophistication inspired by Diptyque and Boy Smells. Includes a demo banner at the top (this is a proposition for the business owner).

## Color Tokens

| Token | Hex | Usage |
|-------|-----|-------|
| Primary | `#1A1A1A` | Nav background, section dividers, footer, dark sections |
| Secondary | `#763b13` | Headings (Bon Voyage), CTA buttons, numbered badges, accent text |
| Accent | `#C4A882` | Hover states, decorative lines, subtle gold details, overlines |
| Neutral | `#6B6158` | Body text secondary, captions, muted labels |
| Background | `#FAF7F3` | Page background, light sections |
| Text | `#232323` | Primary body text |
| White | `#FFFFFF` | Text on dark backgrounds, card backgrounds |

## Typography

- **Display Font**: Bon Voyage — display headings, section titles, product names. Wide letter-spacing (0.1–0.15em).
- **Secondary Heading Font**: Libre Baskerville — secondary headings, fragrance names, quotes.
- **Body Font**: Neuzeit Grotesk — body text, descriptions, UI elements.
- **Logo Font**: Calligraphic/script — "Lisenza Studio" wordmark only (use LOGO placeholder).

## Page Sections (design each one in order)

### Section 0: Demo Banner
- Full-width bar at very top. Background `#1A1A1A`, text `#C4A882`.
- Content: "Este es un demo de tu nueva página web — Creado por KwiHub"
- Height: 36px. Font: 12px uppercase tracking 0.1em. Dismiss X on the right.

### Section 1: Navigation
- Sticky nav below demo banner. Height: 64px. Background: transparent (over hero).
- Left: "Productos | Aromas | Nuestra Historia" links
- Center: "Lisenza Studio" LOGO placeholder in script font
- Right: ES/EN language toggle, cart icon with badge count

### Section 2: Hero
- Full viewport height (min 800px). Full-bleed atmospheric background: amber glass candles on linen fabric, warm lighting, bokeh. Use G() to generate this.
- Dark gradient overlay from bottom (60% opacity).
- Text positioned bottom-left with 8% left margin:
  - Headline: "Aromas que transforman tus espacios" — Bon Voyage 60px `#FFFFFF`, tracking 0.12em
  - Subheadline: "Velas, difusores y sprays artesanales con cera de soya 100% natural. Hechos a mano en República Dominicana." — 18px `#FAF7F3` at 60% opacity
  - CTA: "Descubre Nuestros Aromas" — outlined 1px `#FFFFFF` border, uppercase 13px tracking 0.15em, 48px height

### Section 3: Product Lines
- Background: `#FAF7F3`
- Overline: "NUESTROS PRODUCTOS" — 12px `#C4A882` uppercase tracking 0.15em
- Title: "Colección Lisenza" — Bon Voyage 42px `#1A1A1A`
- 3-column grid. Each card:
  - Product image placeholder (3:4 ratio) — use G() for "amber glass candle with bamboo lid on white linen background", "amber glass spray bottle on white linen", "amber glass reed diffuser with black reeds on white linen"
  - Name in Bon Voyage 28px `#763b13`
  - Description in 16px `#232323`
  - Size in 14px `#6B6158`
  - Price in Libre Baskerville 22px bold `#1A1A1A`
  - Button: "Agregar al Carrito" — filled `#763b13`, white text, uppercase 12px, 44px height
- Products:
  1. Vela Aromática — "Vela artesanal de 5.5oz en cera de soya 100% natural. Presentada en elegante envase ámbar con tapa de bambú. Disponible en 7 fragancias únicas." — 5.5oz · ~30 horas de quemado — RD$800
  2. Linen & Room Spray — "Spray de 2oz para ambientes y textiles. En frasco ámbar de vidrio, refresca tus espacios y telas sin dejar manchas. Disponible en 7 fragancias únicas." — 2oz — RD$500
  3. Difusor de Varillas de Caña — "Difusor de 2oz con varillas de caña en elegante frasco ámbar. Libera fragancia de forma continua durante 5 a 8 semanas, llenando cada rincón con calidez y armonía." — 2oz · 5–8 semanas — RD$750
- Spacing: 100px padding top/bottom, 32px gap between cards.

### Section 4: Fragrances
- Background: alternating `#FAF7F3` and `#FFFFFF` rows
- Overline: "AROMAS DISPONIBLES" — 12px `#C4A882` uppercase
- Title: "Siete Fragancias Únicas" — Bon Voyage 42px `#1A1A1A`
- Editorial alternating layout — each fragrance gets a full-width row:
  - Odd rows: image left (40%) + text right (60%)
  - Even rows: text left (60%) + image right (40%)
  - Name in Libre Baskerville 24px `#763b13`
  - Description in italic 16px `#232323`
  - Scent notes as pill badges: rounded-full, border 1px `#C4A882`, text `#6B6158`, 12px uppercase
- Use G() for each fragrance image (atmospheric, evocative):
  1. **Lavanda & Ámbar** — "Ámbar egipcio y lavanda francesa en armonía: un aroma sofisticado, sereno y atemporal." — Notes: Lavanda francesa, ámbar egipcio, mirra negra, haba tonka, almizcle egipcio, salvia — G: "French lavender fields at golden hour with amber resin crystals"
  2. **Lino Blanco** — "Como un abrazo de telas recién lavadas, flores suaves y acordes de algodón para llenar tus días en frescura y ligereza cotidiana." — Notes: Cítrico, Melocotón, Lirio, Jazmín, Rosa, Verde, Madera, Ámbar, Almizcle — G: "white linen sheets billowing in soft breeze with white flowers"
  3. **Caoba & Coco** — "Caoba y coco en armonía, suavizados con sándalo y vainilla, realzados por un toque cítrico contemporáneo." — Notes: Limón, Coco, Vainilla, Sándalo, Almizcle — G: "split coconut on dark mahogany wood with vanilla beans"
  4. **Palo Santo & Pachulí** — "Sándalo y pachulí dulce, realzados por especias cálidas, en un aroma elegante y acogedor." — Notes: Pimienta negra, clavo, nuez moscada, Lavanda, pachulí, vainilla, ámbar, sándalo, olíbano — G: "burning palo santo stick with rising smoke and warm spices"
  5. **Vainilla** — "Vainilla mantequillosa, maple dorado y coco tostado en una fragancia dulce y reconfortante." — Notes: Mantequilla, Coco, Vainilla, Arce — G: "vanilla beans with golden maple syrup and toasted coconut shavings"
  6. **Rocío & Té** — "Pepino, lima y flores suaves en una fragancia limpia, fresca y luminosa." — Notes: Naranja, Lima, Hojas verdes, Pepino, Rosa, Jazmín, Almizcle — G: "morning dew on green tea leaves with cucumber slices and lime"
  7. **Eucalipto & Menta** — "Menta verde y eucalipto en una fragancia fresca, herbal y energizante." — Notes: Limón, Eucalipto, Menta verde, Almizcle — G: "eucalyptus branches with fresh spearmint leaves in morning light"
- Spacing: 80px between rows, 120px section padding.

### Section 5: How to Order
- Background: full-width `#1A1A1A` — dramatic dark section
- Title: "¿Cómo Ordenar?" — Bon Voyage 42px `#FFFFFF`
- 3 columns with numbered badges:
  - Badge: square rounded 8px, `#763b13` bg, white number Bon Voyage 24px
  - Title in Libre Baskerville 20px `#FFFFFF`
  - Description in 16px `#FAF7F3` at 80% opacity
- Steps:
  1. Confirmar disponibilidad — "Escríbenos por WhatsApp para confirmar disponibilidad, aroma y presentación."
  2. Realizar pago — "Confirma tu orden realizando el pago vía transferencia (Banco BHD o Banco Popular)."
  3. Coordinar envío — "Completa tus datos de envío. El delivery tiene un costo adicional desde RD$250."
- CTA bottom: "Escríbenos por WhatsApp" — filled `#763b13`, 48px height
- Spacing: 120px padding.

### Section 6: About / Brand Story
- Background: `#FAF7F3`
- Overline: "LISENZA STUDIO" — `#C4A882`
- Title: "Nuestra Historia" — Bon Voyage 42px
- Split 50/50. Left: owner photo placeholder (OWNER_IMAGE). Right: story text.
  - Story: "Lisenza Studio nació de la pasión por transformar espacios cotidianos en experiencias sensoriales. Cada producto es elaborado artesanalmente en República Dominicana con cera de soya 100% natural y fragancias cuidadosamente seleccionadas. Creemos que un buen aroma tiene el poder de cambiar tu día — desde el primer momento que enciendes una vela hasta la última nota que permanece en tu habitación. Nuestro compromiso es ofrecer productos puros, elegantes y accesibles que llenen tu hogar de calidez y armonía."
  - Decorative `#C4A882` 1px vertical line on left edge of text
  - Signature: "— Leslie Terrero, Fundadora" in Libre Baskerville italic 14px `#6B6158`
- Spacing: 120px padding.

### Section 7: Good to Know
- Background: `#FFFFFF`
- Title: "Bueno Saberlo" — Bon Voyage 36px
- 2x2 grid of info cards:
  - Each: icon (line-art `#763b13`) + title Libre Baskerville 18px `#1A1A1A` + description 15px `#6B6158`
  - `#C4A882` left border 3px accent
- Items:
  1. ¿No sabes qué aroma elegir? — "Solicita nuestro kit de mini muestras gratuitas y descubre tu fragancia favorita. Solo pagas el costo de envío hasta tu ubicación."
  2. ¿Regalos? — "¿Tu orden es para obsequiar? Incluimos empaque de regalo sin costo adicional en tu orden."
  3. Facturación — "Si deseas recibir tu factura con comprobante fiscal (NCF), notifícalo al momento de ordenar."
  4. Personalización — "Si deseas adquirir productos personalizados con tu marca o para eventos especiales, contáctanos."
- Spacing: 100px padding, 24px card gap.

### Section 8: Footer
- Background: `#1A1A1A`
- 3 columns:
  - Left: "Lisenza Studio" LOGO, tagline "Aromas artesanales para tus espacios" 14px `#6B6158`
  - Center: WhatsApp (829) 775-6348, Email lisenza.studio@gmail.com, Instagram @lisenza.studio — 14px `#FAF7F3` 70% opacity
  - Right: Social icons (Instagram, WhatsApp, Email) — `#C4A882` 24px
- Bottom: 1px line `#6B6158` 30% opacity. "© 2025 Lisenza Studio. Santo Domingo, República Dominicana." 12px `#6B6158`
- Spacing: 80px top, 40px bottom.

### Section 9: WhatsApp Floating Button
- Fixed bottom-right, 24px from edges. 60px circle. `#25D366` bg, white icon.
- Box-shadow: 0 4px 12px rgba(0,0,0,0.15).
- Tooltip: "Escríbenos"

## Key Directives

- **Primary CTA**: "Descubre Nuestros Aromas" — EXACT text everywhere
- **Business name**: Lisenza Studio — in nav and footer
- **Brand vibe**: Artisanal, cozy, elegant, luxurious, minimal
- **Mood direction**: "Maison Noire" — elevated luxury, high contrast, editorial sophistication

## Brand Assets

### Colors & Fonts
Colors: #763b13 (brown accent), #232323 (base text), #d2b299 (warm beige), #1A1A1A (primary dark), #C4A882 (gold accent), #FAF7F3 (background ivory)
Fonts: Bon Voyage (display), Libre Baskerville (secondary serif), Neuzeit Grotesk (body)

### Brand Assets Location
Logo and photos at: ~/kwilaunch/projects/lisenza-studio/assets/
Files: leslie-terrero-owner-caricatura.jpg, leslie-terrero-owner-picture.jpg, product-apple-cinnamon.jpg, product-caoba-coco.jpg, product-citrus.jpg, product-decorative-candle.jpg, product-dulce-encanto-2.jpg, product-dulce-encanto.jpg, product-lavanda-ambar.jpg, product-lino-blanco.jpg, product-pack-christmas-cookies.jpg, product-pack-citrus-joy.jpg, product-vainilla.jpg, product-velas.jpg, tip-image-about-difusor.jpg

**IMPORTANT**: Do NOT use G() to reproduce logos. Use LOGO placeholder rectangles. For product images in the Products section, try to use the real photos from assets/ via Read() to understand what they look like, then use G() for atmospheric/editorial interpretations.

## Mood Board References
These URLs were curated during mood direction phase:
- https://www.diptyqueparis.com — luxury editorial fragrance house
- https://boysmells.com — modern luxury candles, high contrast
- https://brooklyncandlestudio.com — botanical, refined serif typography

## Target File
The .pen file is located at: ~/kwilaunch/projects/lisenza-studio/design.pen
It should already be open in Pencil.
