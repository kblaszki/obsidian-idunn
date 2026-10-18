---
name: extend-theme
description: Extends the Idunn Obsidian theme by adding or changing CSS tokens, UI chrome, markdown, or syntax highlighting. Use when editing src/*.css, adding colors, tuning code highlighting, or implementing visual theme features.
---

# Extend Idunn theme

## Instructions

1. Read `docs/index.md` and the relevant how-to (`docs/how-to/add-color-token.md` or `tune-syntax-highlighting.md`).
2. Edit the correct module only:

   | Change | File |
   |--------|------|
   | Brand / shared tokens | `src/tokens.css` |
   | Dark surfaces & `--code-*` | `src/dark.css` |
   | Light surfaces & `--code-*` | `src/light.css` |
   | Headings | `src/typography.css` |
   | Quotes, tables, tags, links | `src/markdown.css` |
   | Syntax selectors | `src/code.css` |
   | Tabs, nav, focus | `src/ui.css` |

3. Prefer Obsidian CSS variables; keep brand hex in `--idunn-*`.
4. Update `docs/reference/design-tokens.md` if new tokens are introduced.
5. Run `npm run build` and confirm `theme.css` updated.
6. Ask the user to verify Dark + Light in Obsidian (or note it as required QA).

## Do not

- Hand-edit only `theme.css` without updating `src/`
- Break build module order in `scripts/build.mjs` without updating docs
- Use “Theme” / “Obsidian” in `manifest.json` `name`
