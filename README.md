# Idunn

[![Obsidian Theme](https://img.shields.io/badge/Obsidian-Theme-7a53b8?style=flat-square&logo=obsidian&logoColor=white)](https://obsidian.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

**Idunn** — named after the Norse goddess of spring and renewal — is a clean, modern **Dark & Light** theme for [Obsidian](https://obsidian.md).

Built for developers and technical writers: crystal-clear typography, high-contrast syntax highlighting (especially C++ and Markdown), and a calm palette of ocean blues, cyan, and emerald green that keeps long documentation sessions focused.

---

## Features

- **Dual Mode Support** — carefully crafted **Dark** and **Light** color schemes
- **Developer-Grade Syntax** — readable code blocks with clear contrast for C++ and Markdown
- **Vibrant Accents** — cyan, emerald, and ocean blue on headings and UI chrome
- **Distraction-Free** — modern, airy layout suited to writing, studying, and docs

---

## Screenshots

> Add real captures before submitting to Community Themes (recommended **512×288**, 16:9). See [screenshots/README.md](screenshots/README.md).

| Dark Mode | Light Mode |
|-----------|------------|
| ![Dark mode](screenshots/dark.png) | ![Light mode](screenshots/light.png) |

---

## Installation

### Community Themes (recommended)

Once published:

1. Open **Settings → Appearance → Themes**
2. Select **Manage**
3. Search for **Idunn** and install
4. Enable the theme from the Themes dropdown

### Manual install

1. Download or clone this repository
2. Copy the folder into your vault:

   ```text
   <vault>/.obsidian/themes/Idunn/
   ```

   The folder name must match the theme `name` in `manifest.json` (`Idunn`).

3. Ensure these files are present inside that folder:
   - `manifest.json`
   - `theme.css`
4. In Obsidian: **Settings → Appearance → Themes → Idunn**
5. Restart Obsidian if the theme does not appear after changing `manifest.json`

---

## Development & Customization

Source CSS lives in `src/`; `theme.css` is the built release artifact.

```bash
npm run build    # concatenate src/*.css → theme.css
npm run watch    # rebuild on changes under src/
```

1. Symlink or copy this repo to `<vault>/.obsidian/themes/Idunn/`
2. Edit modules under `src/` (see [docs/reference/file-structure.md](docs/reference/file-structure.md))
3. Run `npm run build` (or `watch`)
4. Reload the theme in Obsidian (toggle theme or restart)

Full guides: **[docs/index.md](docs/index.md)** (Diátaxis map — tutorials, how-tos, reference, explanation).

### Submitting to Community Themes

1. Bump `version` in `manifest.json` (semver `x.y.z`)
2. Run `npm run build` and commit `theme.css`
3. Create a GitHub Release whose **tag matches** `manifest.version`
4. Attach `manifest.json` and `theme.css` as release assets
5. Submit via [community.obsidian.md](https://community.obsidian.md)

Details: [docs/how-to/prepare-community-release.md](docs/how-to/prepare-community-release.md).

---

## License

Distributed under the [MIT License](LICENSE).
