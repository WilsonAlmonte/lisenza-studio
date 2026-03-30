# Design Spec: Lisenza Studio Landing Page

## Overview
A bilingual (ES/EN) e-commerce landing page for Lisenza Studio, an artisanal home fragrance brand in Santo Domingo, Dominican Republic. The page drives online sales through a WhatsApp cart flow — users browse products, add to cart, and checkout via WhatsApp. Visual direction: "Maison Noire" — elevated luxury with high-contrast editorial sophistication inspired by Diptyque and Boy Smells. Includes a demo banner at the top (this is a proposition for the business owner).

## Important Notes
- **Bilingual**: All copy appears in Spanish (primary) and English. Use a language toggle in the nav — default to Spanish.
- **Demo Banner**: Sticky top bar before the nav: "Este es un demo de tu nueva página web — Creado por KwiHub" with a dismiss X.
- **WhatsApp Cart**: Products have "Add to Cart" buttons. Cart icon in nav with badge count. Cart page sends order summary to WhatsApp (829) 775-6348. Reference `~/repos/kwihub/tea-cup/` for the AddToCart/CartBadge/CartPage component pattern.
- **Logo**: Use the "Lisenza Studio" wordmark in calligraphic/script font. There is a logo asset in `assets/` — use LOGO placeholder in design, real file embedded at code phase.

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

- **Display Font**: Bon Voyage — display headings, section titles, product names. Wide letter-spacing (0.1–0.15em), uppercase or title case depending on context.
- **Secondary Heading Font**: Libre Baskerville — secondary headings, fragrance names, quotes. Regular weight, elegant serif.
- **Body Font**: Neuzeit Grotesk — body text, descriptions, UI elements. Clean, modern.
- **Logo Font**: Calligraphic/script — "Lisenza Studio" wordmark only.

### Type Scale
| Element | Size (desktop) | Weight | Tracking |
|---------|---------------|--------|----------|
| H1 (hero) | 56–64px | 400 | 0.12em |
| H2 (section) | 36–42px | 400 | 0.08em |
| H3 (subsection) | 24–28px | 400 | 0.05em |
| Body | 16–18px | 400 | 0.02em |
| Small / Caption | 13–14px | 400 | 0.03em |
| Overline | 11–12px | 500 | 0.15em, uppercase |
| Price | 20–24px | 700 | 0 |

## Tone & Voice
Keywords: sophisticated, luxurious, refined, timeless

The copywriting voice is poetic yet restrained — like a luxury fragrance house catalog. Sentences are short, evocative, and sensory. Avoid exclamation marks. Let the products speak through description rather than hyperbole. Spanish is the primary language; English follows the same elegant tone.

## Page Sections

### 0. Demo Banner
- **Purpose**: Signal this is a proposition/demo, not the live site
- **Content**: "Este es un demo de tu nueva página web — Creado por KwiHub" | "This is a demo of your new website — Created by KwiHub"
- **Layout**: Full-width sticky bar at very top, above nav. Background `#1A1A1A`, text `#C4A882`, dismiss X on the right. Height: 36px. Font: Neuzeit Grotesk 12px uppercase tracking 0.1em.

### 1. Navigation
- **Purpose**: Brand identity + product navigation + language toggle + cart
- **Layout**: Sticky top nav, transparent over hero → solid `#1A1A1A` on scroll. Height: 64px. Logo "Lisenza Studio" centered in script font. Left: hamburger menu (mobile) or links "Productos | Aromas | Nuestra Historia". Right: language toggle (ES/EN), cart icon with badge count.
- **Transition**: Transparent → solid over 200ms at 80px scroll offset. Backdrop blur on solid state.
- **Mobile**: Full-screen overlay from right, dark background, large tap targets (56px height), social links at bottom.

### 2. Hero
- **Purpose**: Emotional first impression — sensory, luxurious, product-forward
- **Headline (ES)**: "Aromas que transforman tus espacios"
- **Headline (EN)**: "Scents that transform your spaces"
- **Subheadline (ES)**: "Velas, difusores y sprays artesanales con cera de soya 100% natural. Hechos a mano en República Dominicana."
- **Subheadline (EN)**: "Handcrafted candles, diffusers & sprays made with 100% natural soy wax. Made by hand in the Dominican Republic."
- **CTA**: "Descubre Nuestros Aromas" / "Explore Our Scents"
- **Layout**: Full-viewport height (100vh). Full-bleed atmospheric product photography as background (amber glass containers on linen, warm lighting). Dark gradient overlay from bottom (60% opacity) for text legibility. Text positioned bottom-left with generous left margin (8%). Headline in Bon Voyage 56–64px `#FFFFFF`. Subheadline in Neuzeit Grotesk 18px `#FAF7F3` with 60% opacity. CTA button: outlined thin 1px `#FFFFFF` border, uppercase Neuzeit Grotesk 13px tracking 0.15em, 48px height, px-10. Hover: fills `#763b13` with white text.
- **Mobile**: Text centered, bottom 30%, CTA full-width with 16px margin.

### 3. Product Lines
- **Purpose**: Showcase the 3 product categories with pricing — this is the shop
- **Overline**: "NUESTROS PRODUCTOS" / "OUR PRODUCTS" — Neuzeit Grotesk 12px `#C4A882` uppercase tracking 0.15em
- **Section Title**: "Colección Lisenza" / "The Lisenza Collection" — Bon Voyage 42px `#1A1A1A`
- **Layout**: 3-column grid on desktop (1 column mobile). Each product is a large card:
  - Product image: 3:4 aspect ratio, amber glass product on clean white/linen background. Use product photos from `assets/` as PRODUCT_IMAGE placeholders.
  - Product name in Bon Voyage 28px `#763b13` (e.g., "Vela Aromática")
  - Description in Neuzeit Grotesk 16px `#232323`
  - Size/specs in Neuzeit Grotesk 14px `#6B6158`
  - Price in Libre Baskerville 22px bold `#1A1A1A`
  - "Agregar al Carrito" / "Add to Cart" button: filled `#763b13`, white text, uppercase 12px tracking 0.1em, 44px height
- **Cards**: No border, subtle shadow on hover (0 4px 20px rgba(0,0,0,0.08)). Hover: image scale 1.03 in 300ms ease.
- **Products**:
  1. **Vela Aromática** — 5.5oz · ~30 horas de quemado — RD$800
  2. **Linen & Room Spray** — 2oz — RD$500
  3. **Difusor de Varillas de Caña** — 2oz · 5–8 semanas — RD$750
- **Spacing**: 100px top/bottom padding. 32px gap between cards.

### 4. Fragrances
- **Purpose**: Showcase the 7 scents with poetic descriptions — the sensory heart of the page
- **Overline**: "AROMAS DISPONIBLES" / "AVAILABLE SCENTS" — `#C4A882`
- **Section Title**: "Siete Fragancias Únicas" / "Seven Unique Fragrances" — Bon Voyage 42px
- **Layout**: Editorial alternating rhythm — each fragrance gets a row. Odd rows: image left (40%) + text right (60%). Even rows: text left (60%) + image right (40%). This creates the Diptyque-style editorial flow.
  - Fragrance name in Libre Baskerville 24px `#763b13`
  - Poetic description in Neuzeit Grotesk 16px italic `#232323`
  - Scent notes as pills/tags: small rounded-full badges, border 1px `#C4A882`, text `#6B6158`, 12px uppercase tracking 0.08em
  - Each fragrance row has a "Select" dropdown to choose product type (Candle/Spray/Diffuser) + "Add to Cart" mini button
- **Background**: Alternating — `#FAF7F3` and `#FFFFFF` rows for subtle visual rhythm
- **Fragrances** (in order):
  1. Lavanda & Ámbar — sophisticated, serene, timeless
  2. Lino Blanco — fresh linens, soft florals, lightness
  3. Caoba & Coco — mahogany, coconut, contemporary citrus
  4. Palo Santo & Pachulí — warm spices, elegant, welcoming
  5. Vainilla — buttery, golden maple, comforting
  6. Rocío & Té — clean, fresh, luminous
  7. Eucalipto & Menta — herbal, energizing
- **Spacing**: 80px padding between fragrance rows. 120px section top/bottom padding.
- **Mobile**: Stack image above text, full width. 60px between rows.

### 5. How to Order
- **Purpose**: Clear 3-step ordering process — reduces friction, builds confidence
- **Background**: Full-width `#1A1A1A` dark section — creates visual break
- **Section Title**: "¿Cómo Ordenar?" / "How to Order?" — Bon Voyage 42px `#FFFFFF`
- **Layout**: 3 columns, each with a numbered badge + title + description
  - Number badges: Square with rounded corners (8px), `#763b13` background, white number in Bon Voyage 24px
  - Step title in Libre Baskerville 20px `#FFFFFF`
  - Step description in Neuzeit Grotesk 16px `#FAF7F3` at 80% opacity
- **Steps**:
  1. **Confirmar disponibilidad** — "Escríbenos por WhatsApp para confirmar disponibilidad, aroma y presentación."
  2. **Realizar pago** — "Confirma tu orden realizando el pago vía transferencia (Banco BHD o Banco Popular)."
  3. **Coordinar envío** — "Completa tus datos de envío. El delivery tiene un costo adicional desde RD$250."
- **CTA at bottom**: WhatsApp button — "Escríbenos por WhatsApp" / "Message Us on WhatsApp" — filled `#763b13`, 48px height
- **Spacing**: 120px top/bottom padding. 48px between step columns.
- **Mobile**: Single column, steps stacked vertically with 40px between.

### 6. About / Brand Story
- **Purpose**: Emotional connection — the craft, the passion, the origin
- **Overline**: "LISENZA STUDIO" — `#C4A882`
- **Section Title**: "Nuestra Historia" / "Our Story" — Bon Voyage 42px
- **Layout**: Split 50/50. Left: owner photo (Leslie Terrero — use `assets/leslie-terrero-owner-picture.jpg` as OWNER_IMAGE placeholder). Right: brand story text.
  - Story text in Neuzeit Grotesk 17px `#232323`, line-height 1.8 for readability
  - A decorative vertical line `#C4A882` 1px on the left edge of the text block
  - Signature or "— Leslie Terrero, Fundadora" at the bottom in Libre Baskerville italic 14px `#6B6158`
- **Story (ES)**: "Lisenza Studio nació de la pasión por transformar espacios cotidianos en experiencias sensoriales. Cada producto es elaborado artesanalmente en República Dominicana con cera de soya 100% natural y fragancias cuidadosamente seleccionadas. Creemos que un buen aroma tiene el poder de cambiar tu día — desde el primer momento que enciendes una vela hasta la última nota que permanece en tu habitación. Nuestro compromiso es ofrecer productos puros, elegantes y accesibles que llenen tu hogar de calidez y armonía."
- **Spacing**: 120px top/bottom.
- **Mobile**: Stack image above text, full width.

### 7. Good to Know
- **Purpose**: Address common questions and value-adds — reduces purchase hesitation
- **Section Title**: "Bueno Saberlo" / "Good to Know" — Bon Voyage 36px
- **Layout**: 2x2 grid of info cards on desktop, single column on mobile
  - Each card: icon (line-art style, `#763b13`) + title in Libre Baskerville 18px `#1A1A1A` + description in Neuzeit Grotesk 15px `#6B6158`
  - Cards have subtle `#C4A882` left border (3px) as accent
  - No background color on cards — they sit on the page background
- **Items**:
  1. **¿No sabes qué aroma elegir?** — Free mini sample kit, pay shipping only
  2. **¿Regalos?** — Free gift wrapping included
  3. **Facturación** — NCF fiscal invoicing available
  4. **Personalización** — Custom branded products for events
- **Spacing**: 100px top/bottom. 24px gap between grid cards.

### 8. Footer
- **Purpose**: Contact info, social links, legal
- **Background**: `#1A1A1A`
- **Layout**: 3-column on desktop
  - Left: "Lisenza Studio" logo in script font `#FAF7F3`, tagline "Aromas artesanales para tus espacios" in Neuzeit Grotesk 14px `#6B6158`
  - Center: Contact info — WhatsApp (829) 775-6348, Email lisenza.studio@gmail.com, Instagram @lisenza.studio — in Neuzeit Grotesk 14px `#FAF7F3` at 70% opacity
  - Right: Social icons (Instagram, WhatsApp, Email) — `#C4A882`, 24px, hover `#FFFFFF`
- **Bottom bar**: 1px line `#6B6158` at 30% opacity. "© 2025 Lisenza Studio. Santo Domingo, República Dominicana." in 12px `#6B6158`
- **Spacing**: 80px top, 40px bottom.
- **Mobile**: Single column, centered.

### 9. WhatsApp Floating Button
- **Purpose**: Always-accessible WhatsApp contact
- **Layout**: Fixed bottom-right, 24px from edges. 60px circle. `#25D366` background, white WhatsApp icon. Box-shadow: 0 4px 12px rgba(0,0,0,0.15). Subtle pulse animation on idle (every 8s). Z-index 50.
- **Tooltip on hover**: "Escríbenos" in Neuzeit Grotesk 12px, dark tooltip.

## Layout Approach
- **Max width**: 1280px centered container for content. Full-bleed for hero, dark sections, and section backgrounds.
- **Grid**: 12-column with 24px gutters on desktop, 16px on mobile.
- **Section spacing**: 100–120px vertical padding on desktop, 64–80px on mobile.
- **Section separation**: Alternating backgrounds (`#FAF7F3` ↔ `#FFFFFF`) with one dark `#1A1A1A` section (How to Order) for dramatic contrast.
- **Editorial rhythm**: Alternating image-left/image-right in the Fragrances section creates visual movement. Products use a clean grid. How to Order uses the dark section for emphasis.
- **Responsive breakpoints**: Mobile 375px, Tablet 768px, Desktop 1280px, Wide 1440px.
- **Interactions**: Fade-in-up on sections (60px offset, 600ms ease). Product cards hover scale 1.03. Nav transparent → solid transition. Smooth scroll to sections.
- **Accessibility**: WCAG AA contrast (4.5:1 body, 3:1 large text). Focus states: 2px solid outline offset 2px. All product images get descriptive alt text with name + price.

## Code Generation Notes
- **Image aspect ratios**: When generating code, add a `<!-- TODO: confirm aspect ratio for this image -->` comment next to every product/owner image so Wilson can verify each one looks good in context before finalizing.

## Anti-Patterns to Avoid
- No auto-playing carousels or sliders
- No generic stock photography — use only Lisenza's real product photos
- No card grid layouts for fragrances — use editorial alternating rows
- No prices hidden behind clicks — all prices visible inline
- No neon or saturated accent colors — stay within the warm luxury palette
- No excessive animations — keep them subtle and purposeful
- No cluttered hero — one headline, one subheadline, one CTA
