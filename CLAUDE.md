# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for **Androikies**, a luxury vacation rental property in Greece. The entire site is a single `index.html` file with embedded CSS and minimal vanilla JavaScript — no build tooling, no dependencies, no framework.

## Running Locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

No build step required. The site is deployment-ready as-is.

## Architecture

**Single-file design:** All markup, styles, and scripts live in `index.html`. Sections are delineated by HTML comments (`<!-- NAV -->`, `<!-- HERO -->`, `<!-- GALLERY -->`, etc.) and corresponding CSS comment blocks.

**Page sections** (HTML comment markers and matching CSS comment blocks):
`NAV` → `HERO` → `INTRO / ABOUT` → `GALLERY` → `FEATURES` → `AMENITIES` → `LOCATION` → `HOW TO GET HERE` → `INSTAGRAM` → `FOOTER`

**CSS custom properties** define the entire color system at `:root`:
- `--stone`, `--sand`, `--cream`, `--white` — neutral tones
- `--sea`, `--sea-dark` — accent blues
- `--ink` — dark text
- `--muted` — secondary text
- `--border` — dividers

**Typography:** Cormorant Garamond (serif, headings) and Raleway (sans-serif, body) loaded from Google Fonts. Fluid sizing via `clamp()`.

**JavaScript** is minimal and non-critical:
- Nav scroll effect (adds `.scrolled` class on scroll)
- Image right-click/drag protection

**Images** in `images/` are aggressively JPEG-compressed for web. The logo (`OliveGrey-01.png`) is currently deleted (tracked in git as a deletion).

## External Links

- Airbnb listing: `https://www.airbnb.com/rooms/670733615757784048`
- Instagram: `https://www.instagram.com/androikies/`
- Contact email placeholder: `mailto:your@email.com`
