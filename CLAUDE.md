# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio website for Scott Lesovic, hosted on GitHub Pages at scottlesovic.com. The site is intentionally minimal with no build system, frameworks, or dependencies.

## Architecture

**Static Site Structure:**
- Single-page HTML site with vanilla CSS and minimal JavaScript
- No build process, bundlers, or preprocessors
- Direct edit-and-deploy workflow via GitHub Pages

**Key Files:**
- `index.html` - Main entry point and only HTML page
- `stylesheets/stylesheet.css` - Primary theme (371 lines, includes responsive breakpoints at 768px and 480px)
- `stylesheets/print.css` - Print-optimized styles
- `stylesheets/pygment_trac.css` - Code syntax highlighting theme
- `javascripts/main.js` - Placeholder (currently unused)
- `CNAME` - GitHub Pages domain configuration for scottlesovic.com
- `params.json` - Page metadata (note: not actively used in current implementation)

**Static Assets:**
- `images/` - Background textures, icons, and decorative elements
- `pgp/key.asc` - PGP public key for Scott Lesovic

**Historical Context:**
- `wp-composer/packages.json` - Archived WordPress Composer package listings (not actively used)

## Development Workflow

**Local Preview:**
```bash
# Serve locally with any static file server
python3 -m http.server 8000
# or
npx serve
```

**Deploy:**
- Push to main branch - GitHub Pages automatically deploys
- No build step required

**Editing:**
- HTML: Edit `index.html` directly
- Styles: Modify files in `stylesheets/`
- Images: Add to `images/` directory

## Code Structure Notes

**CSS Architecture:**
- Uses Meyer Web CSS Reset v2.0
- Mobile-first responsive design with media queries
- Separate print stylesheet for optimized printing
- Pygments-based syntax highlighting for code blocks (though currently unused)

**Analytics:**
- Google Analytics integrated inline in index.html (UA-31856187-1)

**Domain Configuration:**
- Custom domain managed via CNAME file
- Must contain only the domain name without protocol or paths
