# Lisenza Studio — Landing Page

## Stack
- Astro 5 + TypeScript + Tailwind CSS v4
- Icons: astro-icon with lucide set (`<Icon name="lucide:icon-name" />`)
- CSS config via @import "tailwindcss" + @theme block (Tailwind v4, no config file)

## Conventions
- Components in src/components/ (Astro for static, React .tsx only for interactive)
- Content data in src/content/ as JSON — never hardcode copy in templates
- Theme tokens in src/styles/global.css @theme block — never hardcode hex colors
- Max 200 lines per file — split if needed
- Full-bleed sections, no margins between them, no border-radius on sections
- Use <Image> from astro:assets for optimized images
