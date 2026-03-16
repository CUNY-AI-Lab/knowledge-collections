# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Important Rules

- **Always use the frontend-design skill when making changes that impact aesthetics.** This applies to any visual/styling modifications.
- **Never use Co-Authored-By lines in commits.**

## Project Overview

Workshop 2 of a 3-part CUNY AI Lab faculty series (system prompts → knowledge collections → agentic tools). Single-page HTML slide deck, no build system, no dependencies — open `index.html` directly in a browser.

## Architecture

The presentation is a custom deck engine built without any framework.

**Entry point:** `index.html` — all slides live here as `.slide` divs inside `#deck`. Slide content is the source of truth; `SLIDES.md` is a markdown mirror kept in sync manually after edits.

**JS modules** (loaded at bottom of `index.html` in this order):
- `js/tabs.js` — tab component
- `js/carousel.js` — auto-advancing image carousel
- `js/scrubber.js` — scrubber timeline in the nav bar; exposes `updateScrubber(current, total)`
- `js/deck-engine.js` — core navigation engine; exposes `window.deckEngine`, `window.goTo`, `window.next`, `window.prev`

**CSS files:**
- `css/styles.css` — all layout, components, typography, and design tokens
- `css/responsive.css` — breakpoint overrides
- `css/animations.css` — transition/animation definitions

**Inline script** in `index.html` (before JS tags): `copyTemplate(id)` — clipboard copy for drafting station templates.

## Slide Layouts

Each slide uses one layout class:
- `layout-split` — two-column: `.content` (left, light) + `.stage` (right, panel)
- `layout-content` — single-column, light background
- `layout-full-dark` — centered, dark background (roadmap/model slides)
- `layout-divider` — section break, dark, centered large heading
- `layout-grid` — dark background with `.grid-2` card layout

## Progressive Reveal

Two mechanisms, both managed by `deck-engine.js`:

1. **Step reveal** — elements with `class="step-hidden" data-step` are revealed one at a time on each forward advance. Reset when leaving the slide.
2. **Stream bullets** — `<ul class="stream-list">` items animate in with staggered delay (200ms + 250ms per item) when the slide becomes active.

## Conventions

- No em dashes (`—`) anywhere in slide content
- All three discipline examples follow: weak collection → getting warmer → strong collection progression
- Knowledge collection examples must frame the instructor as the curator building a grounded tool, not students uploading their own work
- Drafting station slides: template first, "Your turn" tip-box after
- `SLIDES.md` must be kept in sync with `index.html` after every content edit
- Commit messages: short, lowercase, no sign-off
