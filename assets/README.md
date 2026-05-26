# Assets

This directory holds visual assets used by the top-level `README.md` and
`ARCHITECTURE.md`.

## Status

| File | Current | Notes |
|------|---------|-------|
| `hero.png` | Live screenshot of the English popwiz.ai landing with the hero video paused on a face close-up (1600×900 PNG, ~778 KB) | Re-render by loading `popwiz.ai/?lang=en`, pausing the hero `<video>` at `currentTime ≈ 2.0s` (face close-up frame; t=0/5 are wider body shots, t=8 is a side profile), then capturing the 1600×900 viewport. Run through `pngquant` if size matters. |
| `architecture.svg` | Rendered via mermaid.ink from the source in `../ARCHITECTURE.md` (1831×545 SVG, ~28 KB) | Re-render by passing the mermaid block through any compatible renderer (`mermaid.live`, `mermaid.ink`, `mmdc`) after editing the source. |

Grep marker for any unreplaced placeholder anywhere in the repo:

```bash
grep -rn 'TODO' /d/Projects/POPWIZ_public --include='*.md' --include='*.svg'
```
