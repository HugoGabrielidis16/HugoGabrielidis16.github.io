# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio website for Hugo Gabrielidis, built with vanilla HTML, CSS, and JavaScript. The site showcases his background as a PhD student and ML researcher at CentraleSupélec/Paris-Saclay.

## Architecture

**Single-Page Application Structure:**
- `index.html` - Main HTML file containing all sections (hero, about, projects, contact)
- `css/style.css` - Complete styling including responsive design and animations
- `js/script.js` - Interactive features and DOM manipulation
- `images/` - Profile photo and project assets
- `mystuff/` - Contains source materials (Resume.pdf)

**Section Layout:**
The website follows a vertical single-page design with sections:
1. **Hero** - Profile photo, name, title, and call-to-action buttons
2. **About** - Personal bio, technical skills grid, education/experience cards
3. **Projects** - Grid of research projects and portfolio items
4. **Contact** - Centered contact information (no form)

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
- Test mobile navigation toggle functionality

## Key Implementation Details

**Responsive Design:**
- Mobile-first approach with breakpoints at 768px and 480px
- Mobile hamburger menu implemented in JavaScript
- CSS Grid and Flexbox for adaptive layouts

**Navigation:**
- Fixed navbar with smooth scrolling to sections
- Active link highlighting based on scroll position
- Mobile menu toggle with overlay behavior

**Styling Approach:**
- CSS custom properties for consistent theming
- Gradient backgrounds and modern card-based layouts
- Hover effects and transitions for interactivity
- Profile photo styling with circular crop and shadow effects

**Personal Content:**
- All personal information is populated from Resume.pdf
- Contact section uses real contact information
- Project cards reflect actual research work and GitHub repositories

## Hosting Considerations

This is a static site suitable for:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

The site requires no build process or server-side functionality.