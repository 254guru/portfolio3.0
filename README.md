# Portfolio 3.0

A modern, single-page developer portfolio built with plain HTML, CSS, and JavaScript.

This project is intentionally lightweight:
- No build step
- No framework dependencies
- Fast local iteration
- Easy static deployment

## Overview

This site presents a full personal-brand landing experience with:
- Fixed navigation
- Hero section with animated reveal elements
- Skills visualization with animated progress bars
- Project showcase cards
- Process and testimonial sections
- Call-to-action area and footer

The codebase is now separated by concern:
- `index.html`: page structure and content
- `style.css`: complete styling, layout, animations, and responsive behavior
- `script.js`: interaction logic (skills observer + smooth scrolling)

## Tech Stack

- HTML5
- CSS3 (custom properties, grid, flexbox, keyframes, media queries)
- Vanilla JavaScript (IntersectionObserver, event listeners)
- Google Fonts (Syne + DM Sans)

## Project Structure

.
├── index.html
├── style.css
├── script.js
└── README.md

## Getting Started

### 1) Open locally

Because this is a static site, you can run it directly in your browser:
- Open `index.html` in a browser

For best results (and to avoid potential browser file-policy edge cases), use a local server:

Option A: Python

```bash
python3 -m http.server 8080
```

Then open:
- http://localhost:8080

Option B: VS Code Live Server extension

- Right-click `index.html`
- Choose "Open with Live Server"

## How It Works

## HTML (`index.html`)

Contains semantic section blocks for:
- Availability strip
- Navigation
- Hero
- Tech logos
- Value proposition and skills
- Projects grid
- Process
- Testimonials
- CTA
- Footer

External assets are loaded via:
- `<link rel="stylesheet" href="./style.css"/>`
- `<script src="./script.js"></script>`

## CSS (`style.css`)

Main responsibilities:
- Design tokens in `:root` (colors, radii)
- Layout primitives (`container`, section spacing, grids)
- Typography and button system
- Card, logo, and badge styling
- Keyframe animations (`pulse-dot`, `fadeUp`)
- Mobile responsiveness at `max-width: 768px`

### Key styling areas to customize quickly

- Brand colors: update variables in `:root`
  - `--accent`
  - `--accent2`
  - `--ink`
  - `--page`
- Typography scale:
  - `h1`, `.work-headline`, `.cta-headline`
- Spacing system:
  - section padding rules
  - card padding values

## JavaScript (`script.js`)

Contains two interaction behaviors:

1. Skill bar animation on scroll
- Uses `IntersectionObserver`
- Watches `.skills-box`
- Animates each `.skill-fill` width once the section is visible

2. Smooth-scroll anchor navigation
- Captures clicks for internal links beginning with `#`
- Uses `scrollIntoView` for smooth section navigation

## Content Editing Guide

## Personal details

Update these directly in `index.html`:
- Name/branding text
- Project descriptions
- Testimonials
- Footer copyright
- Contact links (`mailto`, GitHub, LinkedIn, Calendly)

## Skill levels

Adjust inline width percentages in `.skill-fill` elements, for example:

```html
<div class="skill-fill" style="width:94%"></div>
```

## Project cards

Each project card can be updated in place:
- Card title
- Tags
- Description
- Metric
- Link target in `href`

## Accessibility and UX Notes

Current strengths:
- Clear heading hierarchy
- Large touch-friendly CTA buttons
- Visual hover/focus affordances for major actions

Recommended improvements:
- Add explicit `aria-label` where link text is ambiguous
- Add a visible skip-to-content link
- Add reduced-motion handling for users who prefer less animation
- Verify contrast ratios after any color changes

## Performance Notes

The site is already lightweight and should load quickly.

If you continue optimizing:
- Compress and self-host fonts (optional)
- Minify CSS/JS for production (optional)
- Replace emoji placeholders with optimized SVG assets if needed

## Deployment

This project works on any static host.

## Netlify

- Drag and drop the project folder in Netlify dashboard
- Or connect the repository and set publish directory to project root

## Vercel

- Import the repository
- Framework preset: Other
- No build command needed
- Output directory: project root

## GitHub Pages

- Push to GitHub
- In repository settings, enable Pages from the main branch root

## Maintenance Checklist

When making updates:
- Keep content changes in `index.html`
- Keep visual changes in `style.css`
- Keep behavior changes in `script.js`
- Test desktop and mobile breakpoints
- Validate external links
- Check console for JavaScript errors

## Future Enhancements

Possible next steps:
- Add real project screenshots
- Add form backend integration
- Add dark/light theme toggle
- Add structured data for SEO
- Add analytics and event tracking

## License

Use and modify freely for personal portfolio purposes.
If publishing publicly, replace personal identity/contact details with your own.
