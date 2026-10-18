# Reference: file structure

**Scope:** Paths and responsibilities in this repository.  
**When to use:** Locating where to edit CSS, docs, or release metadata.

## Root (Community Themes requirements)

| Path | Role |
|------|------|
| `manifest.json` | Theme metadata (`name`, `version`, `minAppVersion`, `author`) |
| `theme.css` | Built CSS shipped in GitHub Releases |
| `README.md` | Public listing / install docs |
| `LICENSE` | MIT |
| `screenshots/` | Store + README images |

## Source & build

| Path | Role |
|------|------|
| `src/tokens.css` | Shared `--idunn-*` and cross-mode tokens |
| `src/dark.css` | `.theme-dark` variables |
| `src/light.css` | `.theme-light` variables |
| `src/typography.css` | Heading scales and colors |
| `src/markdown.css` | Quotes, tables, tags, links, callouts |
| `src/code.css` | Code blocks and syntax selectors |
| `src/ui.css` | Ribbon, tabs, nav, focus |
| `scripts/build.mjs` | Concatenate modules → `theme.css` |
| `package.json` | `npm run build` / `watch` |

## Build order

`tokens` → `dark` → `light` → `typography` → `markdown` → `code` → `ui`

## Cursor / docs

| Path | Role |
|------|------|
| `docs/` | Diátaxis documentation |
| `.cursor/rules/` | Persistent agent rules |
| `.cursor/skills/` | Task skills (`extend-theme`, `release-theme`, `audit-theme`) |
