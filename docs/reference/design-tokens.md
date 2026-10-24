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
