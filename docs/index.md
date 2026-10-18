# Idunn documentation map

**Scope:** Navigation for humans and AI agents working on the Idunn Obsidian theme.  
**When to use:** Start here to pick the right doc type (Diátaxis). Prefer short how-tos for tasks; use reference for facts.

## Diátaxis

| Need | Type | Start here |
|------|------|------------|
| Learn by doing (first-time setup) | Tutorial | [tutorials/local-setup.md](tutorials/local-setup.md) |
| Achieve a concrete goal | How-to | [how-to/](how-to/) |
| Look up facts (tokens, files) | Reference | [reference/](reference/) |
| Understand why | Explanation | [explanation/design-principles.md](explanation/design-principles.md) |

## How-to index

- [Add or change a color token](how-to/add-color-token.md)
- [Tune syntax highlighting](how-to/tune-syntax-highlighting.md)
- [Prepare a Community Themes release](how-to/prepare-community-release.md)

## Reference index

- [File structure](reference/file-structure.md)
- [Design tokens](reference/design-tokens.md)
- [CSS variable map](reference/css-variable-map.md)

## Project context (one glance)

- Theme display name: **Idunn** (`manifest.json` → `name`)
- Source CSS: `src/*.css` → build → `theme.css`
- Modes: `.theme-dark` / `.theme-light` + shared `body` tokens
- Audience: developers & technical writers (C++, Markdown)
