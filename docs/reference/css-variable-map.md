# Reference: CSS variable map

**Scope:** Which Obsidian CSS variables Idunn sets, by module.  
**When to use:** Finding the right file before changing UI, markdown, or code chrome.

## By module

| Module | Selectors | Variables / focus |
|--------|-----------|-------------------|
| `tokens.css` | `body` | `--idunn-*`, radius, fonts, accent bindings |
| `dark.css` | `.theme-dark` | backgrounds, text, ribbon, `--code-*` |
| `light.css` | `.theme-light` | same set for light scheme |
| `typography.css` | `body` + heading selectors | `--h1-color` … `--h6-*` |
| `markdown.css` | `body` + rendered markdown | links, blockquote, table, tag, callout |
| `code.css` | `body` + token / CM selectors | `--code-size`, token colors |
| `mermaid.css` | `.mermaid` + LP embeds | center/scale; S5 hybrid via `--idunn-mermaid-*`; gantt `--idunn-mermaid-gantt-*` — see [mermaid-css.md](mermaid-css.md) |
| `ui.css` | `body` + workspace chrome | tabs, nav, dividers, focus |

## Conventions

1. Prefer Obsidian CSS variables over one-off selectors.
2. Mode-dependent colors → `.theme-dark` / `.theme-light`.
3. Mode-independent chrome → `body`.
4. Avoid `:root` unless a variable must live there; prefer `body`.
5. Avoid `!important` unless overriding a known core conflict — document why.

## Discovering more variables

In Obsidian: DevTools (`Ctrl+Shift+I`) → Sources → `app.css`, or inspect an element and note `var(--…)`. Official list: [CSS variables](https://docs.obsidian.md/Reference/CSS+variables).
