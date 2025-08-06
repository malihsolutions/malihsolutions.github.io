# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the MalihSolutions company website repository, a static website hosted on GitHub Pages. The site showcases the company's mobile applications, primarily BuddySplit - an expense splitting app.

## Architecture & Structure

**Static Website Structure:**
- `/index.html` - Main landing page introducing MalihSolutions
- `/product/buddysplit/` - Dedicated product section for BuddySplit app
  - `index.html` - Product landing page with features, screenshots, legal links
  - `app-screenshots/` - Visual assets showing app functionality
  - `buddysplit-privacy-policy.html` & `buddysplit-terms-conditions.html` - Legal documents
  - `transparent_logo.svg` - Brand assets
- `/invite/` - Dynamic invitation pages for app functionality
- `/apple-app-site-association.html` - iOS Universal Links configuration for deep linking

**Key Technical Components:**
- **Universal Links Setup**: Apple App Site Association (AASA) file configured for deep linking to BuddySplit app (Team ID: B843M46GHC, Bundle ID: com.malihsolutions.buddysplit)
- **Responsive Design**: CSS Grid and Flexbox layout with mobile-first approach
- **Design System**: CSS custom properties defining brand colors (`--primary-blue: #5265FF`, etc.)
- **Performance**: Inline CSS, optimized fonts (Inter), SVG graphics

## Development Commands

**Local Development:**
```bash
# Serve locally using Python
python -m http.server 8000
# Navigate to http://localhost:8000

# Alternative: Open files directly in browser
open index.html
open product/buddysplit/index.html
```

**Deployment:**
- Automatic deployment via GitHub Pages on push to `main` branch
- No build process required (static files only)

## Content Management

**Adding New Products:**
1. Create new directory under `/product/[product-name]/`
2. Follow BuddySplit structure pattern
3. Update main `index.html` products grid
4. Add legal documents if required

**Updating BuddySplit Content:**
- Screenshots: Replace files in `/product/buddysplit/app-screenshots/`
- Features: Edit `/product/buddysplit/index.html`
- Legal: Update respective HTML files

**Universal Links:**
- Modify `/apple-app-site-association.html` for new deep link paths
- Ensure appID matches actual iOS app configuration

## Design System

**Brand Colors:**
- Primary Blue: `#5265FF`
- Dark Blue: `#4054E6` 
- Light Blue: `#e0f2f7`
- Text Dark: `#2c3e50`

**Typography:**
- Primary font: Inter (Google Fonts)
- Weights: 300, 400, 600, 700

**Component Patterns:**
- Card-based layouts with hover effects
- Gradient backgrounds
- Consistent padding/margin scale (multiples of 20px)
- Border radius: 12-15px for containers, 6-8px for buttons