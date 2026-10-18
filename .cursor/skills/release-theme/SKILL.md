---
name: release-theme
description: Prepares an Idunn Community Themes GitHub release — version bump, build, tag/asset checklist, and submission steps. Use only when the user explicitly asks to release, publish, bump version, or submit the theme to the Obsidian community.
disable-model-invocation: true
---

# Release Idunn theme

## Instructions

1. Confirm screenshots exist: `screenshots/dark.png`, `screenshots/light.png` (16:9). Warn if missing.
2. Agree the next semver with the user; set `version` in `manifest.json` (and `package.json`).
3. Run `npm run build`. Ensure `theme.css` is committed with source changes.
4. Draft release notes from recent commits / user input.
5. Checklist for the user (or execute if they asked for the GitHub release):

   - [ ] Tag name == `manifest.json` `version`
   - [ ] Assets: `manifest.json`, `theme.css`
   - [ ] README install section still accurate
   - [ ] First submit → [community.obsidian.md](https://community.obsidian.md); later → new release only

6. Point to `docs/how-to/prepare-community-release.md` for full detail.

## Do not

- Force-push tags or skip hooks unless the user explicitly requests it
- Change theme `name` from `Idunn`
- Publish without a matching GitHub Release
