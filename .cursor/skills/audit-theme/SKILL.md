---
name: audit-theme
description: Reviews Idunn CSS and repo readiness against Obsidian theme guidelines — contrast, dual modes, CSS variable usage, and community file checklist. Use when auditing the theme, reviewing CSS quality, checking community readiness, or before a release.
---

# Audit Idunn theme

## Instructions

1. Confirm required community files at repo root: `manifest.json`, `theme.css`, `README.md`, `LICENSE`, screenshots paths documented.
2. Run through visual/CSS health:

   - [ ] Both `.theme-dark` and `.theme-light` define surfaces and text
   - [ ] Accents use `--idunn-*` consistently
   - [ ] `--code-*` readable in both modes (C++ / Markdown sample mentally reviewed)
   - [ ] Prefer variables over deep selector hacks; flag unexplained `!important`
   - [ ] `theme.css` matches `npm run build` output from `src/`
   - [ ] `manifest.json` `name` is `Idunn`; version is `x.y.z`

3. Cross-check `docs/reference/design-tokens.md` against `src/tokens.css`.
4. Report findings as: **Blockers** (community/release), **Contrast/UX**, **Maintainability** — concise bullets with file paths.

## References

- `docs/explanation/design-principles.md`
- [Theme guidelines](https://docs.obsidian.md/Themes/App+themes/Theme+guidelines)
- [Submit your theme](https://docs.obsidian.md/Themes/App+themes/Submit+a+theme)
