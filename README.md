# Khans

A multi-page restaurant website for **Khans** — a halal Pakistani-American fusion concept
(burgers, paratha rolls, lamb chops, wings, loaded fries, brunch, chai & sweets).

Static HTML/CSS/JS — no build step. Deploys to Vercel as-is.

## Pages

| Page | File |
| --- | --- |
| Home | `index.html` |
| Menu | `menu.html` |
| Middlesex location | `middlesex.html` |
| Manhattan location | `manhattan.html` |
| Catering | `catering.html` |
| Contact | `contact.html` |
| Order Online | `order.html` |

## Structure

```
.
├── index.html, menu.html, middlesex.html, manhattan.html,
│   catering.html, contact.html, order.html
├── assets/
│   ├── css/styles.css
│   ├── js/main.js
│   └── img/*.svg        # logo, food illustrations, storefronts, patterns
├── vercel.json          # clean URLs + asset caching
└── README.md
```

## Deploy to Vercel

1. Push this repo to GitHub (already on branch `claude/khans-website-replica-3yhOi`).
2. In Vercel: **New Project → Import** this repo.
3. Framework preset: **Other** (no build command, output dir = root). Deploy.

Or with the CLI:

```bash
npm i -g vercel
vercel        # preview
vercel --prod # production
```

## Notes on imagery

All images are self-contained, hand-built SVG illustrations in `assets/img/` so the site
renders perfectly with zero external dependencies. To use real photography instead, drop a
JPG/PNG in `assets/img/` and point the matching `<img src>` at it (e.g. replace
`burger.svg` with `burger.jpg`). Filenames map 1:1 to dishes (`burger`, `paratha-roll`,
`lamb-chops`, `wings`, `loaded-fries`, `chai`, `falooda`, `halwa-puri`) plus `hero`,
`about`, `catering`, `loc-middlesex`, `loc-manhattan`.

Menu items and prices reflect the concept's lineup; update them in `menu.html` (and the
highlight cards in `index.html`) any time.
