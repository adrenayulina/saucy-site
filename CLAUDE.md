# Saucy — Project Guide

## Overview
Saucy is a personal food & travel guide website by Nayul. It's a static site (no build tools, no framework) — just HTML, CSS, and vanilla JS.

## Project Structure
- `index.html` — The main (and currently only) page. Contains all HTML, CSS (in `<style>`), and JS (in `<script>`).
- `index.html.html` — Duplicate of `index.html` (likely accidental). Prefer editing `index.html`.

## Tech Stack
- Pure HTML/CSS/JS — no build system, no package manager, no framework
- Google Fonts: Cormorant Garamond, Karla, Noto Serif KR
- CSS custom properties for theming (defined in `:root`)
- IntersectionObserver for scroll animations
- Hosted as a static site (likely GitHub Pages)

## Design System
- **Color palette** (CSS vars): `--espresso`, `--walnut`, `--clay`, `--sand`, `--linen`, `--parchment`, `--white`, `--terracotta`, `--olive`
- **Typography**: Cormorant Garamond (headings/display), Karla (body), Noto Serif KR (Korean text)
- **Tone**: Minimal, editorial, warm. No flashy UI — elegant and understated.

## Content Structure
- Hero section with site branding
- About section (personal intro)
- Journey timeline (life story across cities)
- Travel map (SVG world map with 31 country pins)
- City guides — currently only **Seoul** with 5 neighborhoods (Seongsu, Itaewon, Seochon, Insadong, Anguk) and 12 spots
- Coming soon: Taipei, San Francisco

## Conventions
- All CSS is inline in `<style>` — minified, single-line per rule
- All JS is inline in `<script>` at the bottom
- Spot entries follow a consistent pattern: `.spot-type` > `.spot-name` > `.spot-kr` > `.spot-desc` > `.tip` > `.spot-link` > `.spot-details`
- Google Maps links use the Maps Search API format
- Korean text uses Noto Serif KR font
- Spot types use CSS classes: default (eats), `.drink`, `.experience`

## When Making Changes
- Keep the editorial, minimal aesthetic — don't add unnecessary UI elements
- Maintain the existing color palette and typography
- Test responsiveness (mobile breakpoint at 600px)
- Preserve the scroll animation behavior (IntersectionObserver)
- New city guides should follow the Seoul guide structure (city-hero > neighborhoods > spots)
