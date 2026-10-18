# Tutorial: local theme setup

**Scope:** First-time development loop — vault install, build, reload.  
**When to use:** You have never run Idunn from source, or need a clean local environment.

## Prerequisites

- Obsidian desktop
- Git + Node.js (for `npm run build`)
- A vault you can use for testing

## Steps

1. Clone the repo (or open your existing clone).

2. Install the theme into the vault so the folder name matches `manifest.json` `name`:

   ```bash
   # Example symlink (adjust paths)
   ln -s /path/to/obsidian-idunn "/path/to/vault/.obsidian/themes/Idunn"
   ```

   Or copy `manifest.json` and `theme.css` into `.obsidian/themes/Idunn/`.

3. Build CSS:

   ```bash
   npm run build
   ```

4. In Obsidian: **Settings → Appearance → Themes → Idunn**.  
   Restart Obsidian if the theme is missing after a `manifest.json` change.

5. Edit a file under `src/` (e.g. `src/dark.css`), run `npm run build` (or `npm run watch`), then toggle the theme or reload to see changes.

## Verify

- [ ] Theme appears in the Themes dropdown as **Idunn**
- [ ] Dark and Light base schemes both look intentional (not broken defaults)
- [ ] A fenced code block uses Idunn `--code-*` colors

## Next

- Add tokens: [../how-to/add-color-token.md](../how-to/add-color-token.md)
- File map: [../reference/file-structure.md](../reference/file-structure.md)
