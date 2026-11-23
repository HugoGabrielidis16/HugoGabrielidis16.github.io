# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal website for Hugo Gabrielidis, built with plain HTML and CSS (no JavaScript, no build step). Hugo is an AI Scientist at cortAIx Labs, Thales (since September 2026) and completed his PhD in machine learning at CentraleSupélec / Université Paris-Saclay in February 2026.

## Architecture

**Single-column "letter" layout:** every page shares one narrow column (~640px), the same top bar (name on the left; Thoughts · Interests · CV · Email on the right) and a one-line footer.

- `index.html` - Home page: portrait, "Hi, I'm Hugo." and a short prose bio with inline links to papers and projects, followed by short lists (Publications, Writing, Elsewhere)
- `articles.html` - "Thoughts" index listing the articles
- `interests.html` - Personal interests page (currently just a title; content to come)
- `articles/*.html` - Individual articles (paths to shared assets use `../`)
- `css/style.css` - All styling; theme colours and fonts are CSS custom properties in `:root`
- `images/` - Profile photo and other images
- `mystuff/` - Source materials (Resume.pdf, linked as the CV)

The header and footer markup is duplicated in every HTML file; keep them in sync when changing them.

## Development Commands

**Local Development:**
```bash
# Serve the website locally
python -m http.server 8000
# or
npx serve .
```

**Testing:**
- Open `index.html` directly in browser for quick testing
- Use browser developer tools for responsive design testing
- Check narrow widths (below 600px) in the browser's device toolbar

## Key Implementation Details

**Design:**
- Warm off-white background, Source Serif 4 for headings and prose, Inter for UI text (loaded from Google Fonts with system fallbacks)
- Single muted green accent for links
- One breakpoint at 600px; the layout is a single column at all widths, so no mobile menu is needed

**Personal Content:**
- Personal information comes from Resume.pdf and the user's own updates
- Publication and project links point to the real papers and GitHub repositories

## Hosting Considerations

This is a static site suitable for:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

The site requires no build process or server-side functionality.