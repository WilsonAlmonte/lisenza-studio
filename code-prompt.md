You are an expert frontend developer. Your task is to implement a production-ready
Astro 5 landing page by reading the visual design from a Pencil (.pen) file and
generating all code.

## Design Source

The .pen design file is at: ~/kwilaunch/projects/lisenza-studio/design.pen
It should already be open in Pencil. Read it via MCP tools — the .pen is the
single source of truth for layout, text, colors, spacing, and images.

## Project Location

The Astro project is scaffolded at: ~/kwilaunch/projects/lisenza-studio/
Dependencies are installed. global.css has base design tokens.
CLAUDE.md has project conventions — read it first.

## Workflow

1. Read CLAUDE.md — understand all project conventions
2. Read the design via Pencil MCP tools:
   - get_editor_state() — find all page frames
   - batch_get() with readDepth: 3 — read section structure, text, colors, icons
   - get_screenshot() — visually verify what you're implementing
3. Update design tokens in global.css @theme to match .pen colors exactly.
   Install any @fontsource packages needed.
4. Extract content into JSON data files in src/content/ with all text from the design.
   Create Zod schemas in src/content.config.ts. Pages must never have hardcoded copy.
5. Build section by section: Astro component in src/components/ for each section.
   Match exact layout, spacing, colors, typography from the design.
   Use theme tokens — never hardcode hex. Use <Icon name="lucide:icon-name" /> for icons.
6. Assemble pages in src/pages/.
7. Images:
   - Brand assets are at: ~/kwilaunch/projects/lisenza-studio/assets/
   - Copy: cp -r "assets/" "public/assets/"
   - Reference as /assets/filename.ext
   - Use <Image> from astro:assets with object-cover
8. Run pnpm build — verify no errors.

## Important Context

- This is a bilingual page (Spanish primary, English secondary). The design spec mentions a language toggle.
- Content values are in ~/kwilaunch/projects/lisenza-studio/content-values.json — use these for all copy.
- The design spec mentions a WhatsApp cart flow — reference ~/repos/kwihub/tea-cup/ for the AddToCart/CartBadge/CartPage component pattern if the design includes cart functionality.
- Body font should be Work Sans (already installed as @fontsource/work-sans).
- Libre Baskerville is installed for secondary headings.
- Bon Voyage is the display/heading font — if not available as @fontsource, load it from a local/CDN source or use a similar serif.
- Logo assets are in the assets/ folder — use the actual files, not AI-generated reproductions.

## Rules

- The .pen design is the single source of truth
- No hardcoded hex colors — use Tailwind theme tokens
- Full-bleed sections with internal padding, no rounding, flush vertically
- Astro components for static, React only for interactive features
- Content in JSON data files — never hardcode copy
- Max 200 lines per file
