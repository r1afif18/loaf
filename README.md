# loaf

UI preview for loaf — onchain trackers, jeet receipts and predictions on Robinhood Chain.

This is a static single-page preview. No build step, no dependencies, no live data yet.

## Run locally

Open `index.html` in a browser, or serve it:

    npx serve .

## Deploy

Vercel auto-detects this as a static site. No framework preset, no build command,
output directory is the repo root.

## Structure

    index.html            entire UI (markup, styles, mock data)
    favicon.ico           16/32/48 fallback icon
    apple-touch-icon.png  180x180, iOS home screen
    loaf-icon-512.png     512x512, PWA / share cards

## Swap points

- Chain logos live in the `.chain-menu` block. Stable and Arc use placeholder
  monogram tiles — search `placeholder mark` and drop in the official SVGs.
- All UI icons are `<symbol>` definitions in the sprite at the top of `<body>`,
  referenced with `<use href="#i-name">`. Edit a path once, every usage updates.
- Mock data arrays (`feed`, `lb`, `pts`) sit in the script block at the bottom.
