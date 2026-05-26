# Assets

This directory holds visual assets used by the top-level `README.md` and
`ARCHITECTURE.md`.

## Status

| File | Current | Notes |
|------|---------|-------|
| `hero.png` | Live screenshot of the English popwiz.ai landing (1600×900 PNG, ~849 KB) | Update by re-running a 1600×900 capture of the production site (`?lang=en`). If size matters, run through `pngquant`. |
| `architecture.svg` | Rendered via mermaid.ink from the source in `../ARCHITECTURE.md` (1831×545 SVG, ~28 KB) | Re-render by passing the mermaid block through any compatible renderer (`mermaid.live`, `mermaid.ink`, `mmdc`) after editing the source. |

Grep marker for any unreplaced placeholder anywhere in the repo:

```bash
grep -rn 'TODO' /d/Projects/POPWIZ_public --include='*.md' --include='*.svg'
```
