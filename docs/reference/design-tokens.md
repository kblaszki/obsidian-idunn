# Reference: design tokens

**Scope:** Brand and semantic color tokens defined by Idunn.  
**When to use:** Picking a token name or documenting hex values after a palette change.

## Brand (`src/tokens.css`)

| Token | Default | Role |
|-------|---------|------|
| `--idunn-ocean` | `#1a6b9a` | Deep ocean blue |
| `--idunn-cyan` | `#2aa8c4` | Primary accent / links |
| `--idunn-emerald` | `#2d9a6a` | Secondary accent / success |
| `--idunn-cyan-muted` | `#5ebfd4` | Hover / softer cyan |
| `--idunn-emerald-muted` | `#4caf7a` | Hover / softer emerald |

## Shared bindings (`body`)

| Obsidian var | Bound to |
|--------------|----------|
| `--text-accent` | `--idunn-cyan` |
| `--text-accent-hover` | `--idunn-cyan-muted` |
| `--interactive-accent` | `--idunn-emerald` |
| `--interactive-accent-hover` | `--idunn-emerald-muted` |
| `--color-accent` | `--idunn-cyan` |
| `--color-accent-1` | `--idunn-ocean` |
| `--color-accent-2` | `--idunn-emerald` |

## Surfaces (mode-specific)

Defined in `src/dark.css` and `src/light.css`: `--background-primary`, `--background-secondary`, `--text-normal`, `--text-muted`, `--code-*`, etc. See [css-variable-map.md](css-variable-map.md).
