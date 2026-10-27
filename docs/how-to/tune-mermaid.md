# How to: tune Mermaid diagram chrome

**Scope:** Change Idunn Mermaid colors for flowchart, sequence, quadrant, pie, gantt, and timeline.  
**When to use:** After changing brand accents, or when refining diagram look (current baseline: **S5** hybrid).

For the full token tables and selector → color maps, see [Mermaid CSS reference](../reference/mermaid-css.md).

## Where

| Concern | File |
|---------|------|
| Layout (center, max-width) | `src/mermaid.css` (top) |
| Diagram colors | `--idunn-mermaid-*` / `--idunn-mermaid-gantt-*` in `.theme-dark` / `.theme-light` in same file |

Do **not** put Mermaid hex into `tokens.css` unless they become shared brand tokens.

## Current baseline (S5 hybrid)

| Diagram | Source | Look |
|---------|--------|------|
| Flowchart | S3 | Teal node/cluster frames, muted edges |
| Sequence | S4 | Screen-teal actors, lifelines, signals |
| Quadrant | S4 | Screen-teal title/points |
| Pie | S4 | screen-teal → steel → link → muted (legend paired in CSS) |
| Gantt | S5 | `--idunn-mermaid-gantt-*` bars (teal / link / steel / accent). Dark: pre-invert paints + SVG invert for labels. Thinned axis ticks. |
| Timeline | S5 | Panel nodes (`section--1` / `timeline-node`), no SVG invert |

Preview: `previews/mermaid-style-less.html` (`themeVariables`). Obsidian theme uses CSS overrides — pie/quadrant pairing may need DevTools checks after Mermaid upgrades.

## Obsidian quirks (short)

- Most dark Mermaid SVGs: Idunn sets `filter: none`. Gantt (`:has(.grid)`) keeps Obsidian invert; bars use pre-invert `--idunn-mermaid-gantt-*`; text forced to `#111` so invert yields white.  
- HTML labels: set `color` on `foreignObject` / `.nodeLabel`, not only SVG `fill`.  
- Sequence: override `tspan` (`text.actor > tspan`, `.messageText`), not only `text`.  
- Edge-label chips: keep `--idunn-mermaid-label-bg: transparent`.  
- Timeline first lane is often `.section--1` / `.timeline-node`.

Details: [Mermaid CSS — invert model](../reference/mermaid-css.md#obsidian-invert-model).

## Checklist

1. Look up the element in [mermaid-css.md](../reference/mermaid-css.md); edit the matching `--idunn-mermaid-*` (and gantt twin if needed) under the right scheme.  
2. Prefer token edits over new `!important` selectors. Keep flowchart edges (`.edgePath`) separate from sequence (`.messageLine*`).  
3. `npm run build`.  
4. Verify Dark + Light on flowchart, sequence, quadrant, pie, gantt, and timeline.  
5. After copying `theme.css` into the vault, reload Obsidian (or toggle the theme) so Mermaid re-renders.

## Related

- [Mermaid CSS reference](../reference/mermaid-css.md)
- [CSS variable map](../reference/css-variable-map.md)
