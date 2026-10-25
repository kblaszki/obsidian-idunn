# How to: tune Mermaid diagram chrome

**Scope:** Adjust flowchart / sequence / pie / quadrant colors for Idunn Mermaid.  
**When to use:** After changing brand accents, or when refining diagram look (current baseline: **S5** hybrid).

## Where

| Concern | File |
|---------|------|
| Layout (center, max-width) | `src/mermaid.css` (top) |
| Diagram colors | `--idunn-mermaid-*` in `.theme-dark` / `.theme-light` in same file |

Do **not** put Mermaid hex into `tokens.css` unless they become shared brand tokens.

## Current baseline (S5 hybrid)

| Diagram | Source | Look |
|---------|--------|------|
| Flowchart | S3 | Teal node/cluster frames, muted edges |
| Sequence | S4 | Screen-teal actors, lifelines, signals |
| Quadrant | S4 | Screen-teal title/points, steel internal axes |
| Pie | S4 | screen-teal → steel → link → muted (legend paired in CSS) |
| Gantt | S5 | `--idunn-mermaid-gantt-*` bars (teal / link / steel / accent). Dark: pre-invert paints + SVG invert for labels. Thinned axis ticks. |
| Timeline | S5 | Panel nodes (`section--1` / `timeline-node`), no SVG invert |

Preview: `previews/mermaid-style-less.html` (`themeVariables`). Obsidian theme uses CSS overrides — pie/quadrant pairing may need DevTools checks after Mermaid upgrades.

## Obsidian quirks

- Dark mode applies `filter: invert()` on Mermaid SVG; Idunn sets `filter: none` so panels stay dark and labels light.  
- Node/edge text is often HTML (`foreignObject` / `.nodeLabel`) — set `color`, not only SVG `fill`.  
- Sequence labels use SVG `tspan` (`text.actor > tspan`, `.messageText`) — override those, not only `text`.  
- Gantt dark mode: SVG `filter: invert(…)` on `:has(.grid)`, force text/`tspan` fill to `#111` (invert → white), and paint bars/sections with `--idunn-mermaid-gantt-*` pre-invert light-family hex so the filter yields Idunn teal/steel/blue chrome. Timeline stays painted (no invert).  
- Gantt axis: hide 2/3 of `.grid .tick` labels so dates don’t collide.  
- Timeline first lane is often `.section--1` / `.timeline-node`.  
- Empty/branch edge-label rects: keep `--idunn-mermaid-label-bg: transparent`.

## Checklist

1. Edit `--idunn-mermaid-*` under the right scheme only.  
2. Keep flowchart edges (`.edgePath` / `.flowchart-link`) separate from sequence (`.messageLine*`).  
3. `npm run build`.  
4. Verify Dark + Light on flowchart, sequence, quadrant, pie, gantt, and timeline.  
5. Prefer token edits over new `!important` selectors.  
6. After copying `theme.css` into the vault, reload Obsidian (or toggle the theme) so Mermaid re-renders.

## Related

- [../reference/css-variable-map.md](../reference/css-variable-map.md)
- Vault samples: `50 Diagram Samples/`
