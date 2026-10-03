# Buku — product deck

A public, single-page HTML deck for **Buku**, a product of Right-Jet. The language is Bahasa Indonesia. It has no build step and no dependencies. `index.html` holds the markup, CSS and JS, and the only external request is Google Fonts.

## Present or share

- **Local:** open `index.html` in a browser, or run `python3 -m http.server --directory deck 8000`.
- **Keys:** `←` `→` (or space) move between slides, `F` toggles fullscreen, `Home` and `End` jump to the first and last slide. On touch screens, swipe sideways.
- **PDF:** print from the browser with *Background graphics* on. It prints one slide per page, landscape.
- **Public URL:** enable GitHub Pages for this repo (Settings → Pages → *Deploy from a branch* → branch root). The deck is then served at `/<repo>/deck/`. A `.nojekyll` file is included. Any static host works as well (Vercel, Netlify, Cloudflare Pages), pointed at the `deck/` folder.

## Edit

- **Demo contact:** change the `CONTACT` constant at the top of the `<script>` in `index.html`. It currently points to a placeholder email. Every "Jadwalkan demo" button reads from it.
- **Copy:** each slide is one `<section class="slide">`. Headlines marked `data-split` get the blur-in text effect.
- **Illustrations:** these are inline SVG, drawn with invented data (such as "Contoh Klien"). They contain no real client names or figures.

## Effects

The effects are written from scratch in vanilla JS, CSS and WebGL, in the style of [React Bits](https://reactbits.dev/) components: Aurora, Dot Grid, Blur Text, Gradient and Shiny Text, Spotlight Card, Magnet, Tilted Card, Count Up, and a scrolling marquee. All of them switch off under `prefers-reduced-motion`, and the animated canvases pause while off screen.

## Keep it public-safe

Before editing, remember that this folder is published as-is. Don't add:

- real client names or screenshots of real data
- keys or environment values
- internal URLs or repository details
- QA or security findings
- pricing or claims that the product docs don't back up
