# Reference: design tokens

**Scope:** Brand and semantic color tokens defined by Idunn.  
**When to use:** Picking a token name or documenting hex values after a palette change.

## Brand (`src/tokens.css` + light overrides)

Dark defaults live on `body`; `.theme-light` overrides the five brand tokens.

| Token | Dark | Light | Role |
|-------|------|-------|------|
| `--idunn-ocean` | `#0e6cb8` | `#1d4ed8` | Interactive accent / depth |
| `--idunn-cyan` | `#5eb6f5` | `#2563eb` | Links / secondary blue |
| `--idunn-emerald` | `#3db8a0` | `#0d9488` | Teal brand / success / H2 |
| `--idunn-cyan-muted` | `#8dceff` | `#1e3a8a` | Link hover |
| `--idunn-emerald-muted` | `#5ecfb8` | `#2dd4bf` | Soft teal |

## Shared bindings (`body`)

| Obsidian var | Bound to |
|--------------|----------|
| `--text-accent` | `--idunn-cyan` |
| `--text-accent-hover` | `--idunn-cyan-muted` |
| `--interactive-accent` | `--idunn-ocean` |
| `--interactive-accent-hover` | `--idunn-cyan` |
| `--color-accent` | `--idunn-cyan` |
| `--color-accent-1` | `--idunn-ocean` |
| `--color-accent-2` | `--idunn-emerald` |

## Surfaces (mode-specific)

Defined in `src/dark.css` and `src/light.css`: `--background-primary`, `--background-secondary`, `--text-normal`, `--text-muted`, `--code-*`, etc. See [css-variable-map.md](css-variable-map.md).

### Light surfaces (mist parchment)

| Variable | Hex |
|----------|-----|
| `--background-primary` | `#eef0f2` |
| `--background-secondary` | `#e3e7ec` |
| `--background-secondary-alt` | `#d6dce4` |
| `--background-modifier-border` | `#bcc4cf` |
| `--background-modifier-form-field` | `#f4f5f7` |
| `--code-background` | `#e3e7ec` |

## UI / plugins (`src/ui.css`)

| Concern | Variables |
|---------|-----------|
| Status bar | `--status-bar-background`, `--status-bar-border-color`, `--status-bar-text-color` |
| Graph | `--graph-text`, `--graph-line`, `--graph-node`, `--graph-node-focused`, `--graph-node-tag`, `--graph-node-attachment`, `--graph-node-unresolved` |
| Canvas | `--canvas-background`, `--canvas-dot-pattern`, `--canvas-card-label-color`, `--canvas-color-1`…`6` |

## Markdown chrome (`src/markdown.css`)

Bound on `body` to Obsidian variables (both modes inherit; callout **type** RGB lives in `dark.css` / `light.css`):

| Concern | Variables |
|---------|-----------|
| Callout chrome | `--callout-border-width`, `--callout-radius`, `--callout-border-opacity`, `--callout-padding` |
| Tasks | `--checkbox-color`, `--checkbox-border-color`, `--checkbox-marker-color`, `--checklist-done-*` |
| Properties | `--metadata-background`, `--metadata-border-*`, `--metadata-label-*`, `--metadata-input-*` |
| Embeds | `--embed-background`, `--embed-border-start`, `--embed-padding` |

## Mermaid (`src/mermaid.css`)

Diagram-only tokens live on `.theme-dark` / `.theme-light` in `mermaid.css`, not in `tokens.css`. Hex tables, selector maps, and gantt pre-invert rules: [mermaid-css.md](mermaid-css.md).

| Family | Examples |
|--------|----------|
| Diagram chrome | `--idunn-mermaid-panel`, `--idunn-mermaid-fg`, `--idunn-mermaid-teal`, `--idunn-mermaid-screen-teal`, `--idunn-mermaid-steel`, `--idunn-mermaid-blue`, `--idunn-mermaid-link`, … |
| Gantt paints | `--idunn-mermaid-gantt-panel`, `--idunn-mermaid-gantt-teal`, `--idunn-mermaid-gantt-link`, … |
