# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static website for the "Modern ML in Chemistry" summer school (August 3-5, 2026, University of Leipzig). Hosted via GitHub Pages at `ml4chem2026.github.io`. Funded by COST Action DAEMON (CA22154).

## Architecture

Single-page static site, no build tools or frameworks:
- `index.html` -- all content in one file with anchor-link navigation
- `style.css` -- all styling, responsive design with CSS Grid/Flexbox
- `assets/img/` -- COST and EU logos (official versions from cost.eu and EC)

Fonts loaded via Google Fonts CDN (Inter for body, Space Grotesk for headings). Hero section has a canvas-based molecular network animation and scroll-reveal animations via IntersectionObserver, both in inline `<script>` at the bottom of `index.html`.

## Development

Open `index.html` directly in a browser -- no server needed. Everything works offline except Google Fonts (falls back to system sans-serif).

## Deployment

- `draft` branch: for review, not served by GitHub Pages
- `main` branch: GitHub Pages auto-serves `*.github.io` repos from main. Merging `draft` into `main` makes the site live.
- Do NOT push directly to `main` without confirmation -- the site goes public immediately.

## Content guidelines

- Speakers: only list confirmed speakers (not invited/unconfirmed). Use "Prof. Dr." for all professors regardless of junior/full distinction.
- COST/EU logos: required by funding rules. Use official white-on-transparent versions in the dark footer (no CSS filter hacks). Source files are in `assets/img/`.
- The org/repo name may change pending a naming review (to avoid conflict with the existing ML4Chem Python package).
