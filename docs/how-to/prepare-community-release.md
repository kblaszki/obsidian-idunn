# How to: prepare a Community Themes release

**Scope:** Ship a version installable from Obsidian’s community directory.  
**When to use:** First publish or any new version after visual/CSS changes.

## Prerequisites

- GitHub repo with `README.md`, `LICENSE`, `manifest.json`, `theme.css`
- Screenshots: `screenshots/dark.png`, `screenshots/light.png` (16:9, ~512×288)
- Obsidian + GitHub accounts linked at [community.obsidian.md](https://community.obsidian.md)

## Checklist

1. Update `version` in `manifest.json` (semver `x.y.z` only).
2. Align `package.json` `version` with the manifest (optional but recommended).
3. Run `npm run build` and commit the updated `theme.css`.
4. Confirm folder name for local installs is `Idunn` (matches `name`).
5. Create a GitHub Release:
   - Tag **exactly** equals `manifest.json` → `version`
   - Attach **`manifest.json`** and **`theme.css`** as binary assets
6. First submit only: add the theme via the community directory UI.
7. Later versions: bump + new release; Obsidian picks up matching tags automatically.

## Common failures

| Symptom | Likely cause |
|---------|----------------|
| Theme not installing | Release tag ≠ `version`, or assets missing |
| Wrong name in store | `name` in manifest (cannot include “Theme” / “Obsidian”) |
| Empty store preview | Missing or wrong-aspect screenshot |

## Official docs

- [Submit your theme](https://docs.obsidian.md/Themes/App+themes/Submit+a+theme)
- [Manifest](https://docs.obsidian.md/Reference/Manifest)
