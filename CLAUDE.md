# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static marketing website for the Sun Exposure iOS app, deployed via GitHub Pages at sunexposure.app. The site is built with pure HTML/CSS—no build tools, frameworks, or dependencies required.

## Architecture

### Pages
- `index.html` - Main marketing page (hero, features, download CTAs)
- `privacy-policy/index.html` - Privacy policy page
- `terms-of-use/index.html` - Terms of use page

### Structure
All pages follow a consistent pattern:
1. Shared header with navigation (logo, links, CTA)
2. Page-specific content sections
3. Shared footer with legal links and copyright
4. Single stylesheet (`styles.css`) defines all styling via CSS variables

### Design System
CSS variables in `styles.css:8-18` define the color palette and shadows:
- Primary: `--primary-color` (#FF9500, orange)
- Premium features: `--premium-gradient` (purple gradient)
- Layout: `--dark-color`, `--light-color`, `--text-dark`, `--text-light`

### App Store Integration
- App ID: 6463570196
- Meta tag at `index.html:6` enables Smart App Banner on iOS
- Download links throughout point to `https://apps.apple.com/app/id6463570196`

### Feature Categorization
Features are split into Free and Premium tiers:
- Free features: Use `.badge.free` (green) in `index.html:58-80`
- Premium features: Use `.feature-card.premium` with `.badge.premium-badge` (purple gradient) in `index.html:82-122`

## Common Development Tasks

### Testing Changes Locally
Open HTML files directly in a browser. No local server required:
```bash
open index.html
```

### Deploying to GitHub Pages
This repository auto-deploys via GitHub Pages. Push to `main` branch to deploy:
```bash
git add .
git commit -m "Update content"
git push origin main
```

Site deploys to: https://sunexposure.app (custom domain via CNAME file)

### Adding Images
Place images in `images/` directory. Reference them with relative paths:
```html
<img src="images/filename.png" alt="Description">
```

Current screenshot: `images/screenshot.png` is displayed in phone mockup at `index.html:42`

## Styling Guidelines

### Responsive Breakpoints
- Desktop: default styles
- Tablet: `@media (max-width: 968px)` at `styles.css:436`
- Mobile: `@media (max-width: 768px)` at `styles.css:478`
- Small mobile: `@media (max-width: 480px)` at `styles.css:510`

### Component Patterns
- Hero sections: `.hero` with 2-column grid (content + image)
- Feature cards: `.feature-card` in `.features-grid` (responsive grid)
- Download buttons: `.download-button` with Apple icon SVG
- Footer: 3-column grid on desktop, stacks on mobile

### Legal Pages Structure
Privacy policy and terms pages follow the same structure as `index.html` but with content-focused layout instead of marketing sections. Use the same header and footer for consistency.

## Important Notes

- **No Build Process**: This is static HTML/CSS. Edit files directly and refresh browser to see changes.
- **Apple Design Language**: The site uses Apple's SF Pro font stack and follows iOS design patterns (rounded corners, shadows, clean typography).
- **Custom Domain**: The CNAME file points to `sunexposure.app`. Changes to domain require DNS configuration updates.
- **App Requirements**: All mentions of the app should note "Requires Apple Watch with watchOS 10 or later"
