# AGENTS.md — SoulRockers Coming Soon

Static coming-soon placeholder page for soulrockers.org (launching Sept 3, 2026).
Single `index.html` with inline CSS + JS. No build process, no dependencies.

## Commands

```
# No build step. Open index.html in a browser, or:
python3 -m http.server 8080    # local preview
```

- GitHub Pages serves this at `soulrockers.org` via the `CNAME` file.
- Push to `main` triggers GitHub Pages deploy.

## Structure

```
CNAME                  — custom domain: soulrockers.org
index.html             — single self-contained page (inline CSS + JS)
assets/
  logo.png             — SoulRockers logo (847KB)
  wake-up-mama.mp3     — background music (5.7MB)
```

## Features

- Countdown timer to Sept 3, 2026
- Email signup via Formspree (`mwvdgkkk`)
- Crypto donate modal (BTC/ETH/XMR — addresses hardcoded in JS)
- Audio toggle for background music
- Responsive, dark theme with gold accent (`#d4af37`)

## Gotchas

- **Everything is inline** — CSS in `<style>`, JS in `<script>`. No bundler, no external files beyond assets/.
- **Formspree endpoint** is hardcoded: `https://formspree.io/f/mwvdgkkk`. Changing it requires editing `index.html`.
- **Crypto addresses are in the JS** — `COINS` object near bottom of `<script>`. Update all three (BTC/ETH/XMR) together.
- **Launch date** is hardcoded: `new Date("2026-09-03T00:00:00")`. Update after launch.
- **No `AGENTS.md` convention** needed — this is a trivial static site. This file exists for completeness.
- **This repo is public** — all assets and code are visible. Don't commit secrets.
