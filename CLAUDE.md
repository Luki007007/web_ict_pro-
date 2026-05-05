# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static educational website for **ICT pro** – a Czech IT training agency. The site is deployed on **GitHub Pages** with no build step, no framework, and no package manager.

- **Live URL:** `https://luki007007.github.io/web_ict_pro-/`
- **GitHub repo:** `https://github.com/Luki007007/web_ict_pro-.git`

## Deployment

Push to `main` branch → GitHub Pages auto-deploys. No build command needed.

```powershell
git add <files>
git commit -m "message"
git push
```

The `.nojekyll` file in the root must remain – it prevents GitHub Pages from running Jekyll processing.

## File Structure & Architecture

| File | Purpose |
|---|---|
| `index.html` | Main landing page – hero, course cards, testimonials, CTA, footer |
| `kurz-powerbi.html` | Power BI course detail page |
| `kurz-claude.html` | Claude AI programming course detail page |
| `kurz-tsql.html` | T-SQL course detail page |
| `style.css` | Global styles (navbar, hero, course cards, footer, responsive) |
| `kurz.css` | Styles shared across all three course detail pages |
| `main.js` | Minimal JS – navbar scroll shadow + mobile hamburger menu |

## CSS Architecture

`style.css` defines CSS custom properties on `:root` for the three brand colors:
- `--blue` (#2563eb) – Power BI course
- `--purple` (#7c3aed) – Claude course  
- `--teal` (#0d9488) – T-SQL course

Course cards use `data-color="blue|purple|teal"` attribute to switch accent colors via CSS attribute selectors. The same pattern applies in `kurz.css` with `.module-purple`, `.outcome-teal`, `.btn-termin-purple`, etc.

## Course Page Pattern

All three `kurz-*.html` files share the same layout: navbar → `.kurz-hero` (color-coded) → `.kurz-body` with a two-column grid (`.kurz-main` + `.kurz-sidebar`). When adding a new course page, follow this pattern and assign one of the three hero color classes (`kurz-hero-blue`, `kurz-hero-purple`, `kurz-hero-teal`).

### Course overview

| Course | File | Color | Price | Format | Duration |
|---|---|---|---|---|---|
| Analýza dat – Power BI | `kurz-powerbi.html` | blue | 9 900 Kč | 2-day intensive | 24 h / 8 modules |
| Programování pomocí Claude | `kurz-claude.html` | purple | 8 900 Kč | weekly online (18–20h) | 20 h / 6 modules |
| T-SQL snadno a rychle | `kurz-tsql.html` | teal | 7 900 Kč | 3-day intensive | 18 h / 7 modules |

All prices are without VAT (bez DPH), with instalment option (možnost splátek).

## Hero Floating Cards

The three animated cards in the hero section (`index.html`) are `<a>` elements (not `<div>`), each linking directly to a course page. They have `z-index: 2` so they sit above the decorative `.hero-circle`. On hover, animation pauses and a blue border appears. Do not convert them back to `<div>` – they must remain links.

## Language

All user-facing content is in **Czech**. Keep new content in Czech.
