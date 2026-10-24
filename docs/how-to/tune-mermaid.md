# How to: tune Mermaid diagram chrome

**Scope:** Adjust flowchart / sequence / pie colors for Idunn Mermaid.  
**When to use:** After changing brand accents, or when refining diagram look (current baseline: **M5** teal/blue frames).

## Where

| Concern | File |
|---------|------|
| Layout (center, max-width) | `src/mermaid.css` (top) |
| Diagram colors | `--idunn-mermaid-*` in `.theme-dark` / `.theme-light` in same file |

Do **not** put Mermaid hex into `tokens.css` unless they become shared brand tokens.

## Current baseline (M5)

- Node fill: panel gray; stroke: teal  
- Edges / arrowheads: blue  
- Actors: accent blue border  
- Pie series: teal → blue → accent → link (legend swatches paired in CSS)

Preview experiments: `previews/mermaid-idunn.html` (uses Mermaid `themeVariables`; Obsidian theme uses CSS overrides — pie pairing may need DevTools checks after Mermaid upgrades).

## Checklist

1. Edit `--idunn-mermaid-*` under the right scheme only.  
2. `npm run build`.  
3. Verify Dark + Light on flowchart, sequence, and pie (slice **and** legend).  
4. Prefer token edits over new `!important` selectors.

## Related

- [../reference/css-variable-map.md](../reference/css-variable-map.md)
- Vault samples: `50 Diagram Samples/`
