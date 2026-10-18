# How to: add or change a color token

**Scope:** Introduce a brand or semantic color and wire it into Obsidian CSS variables.  
**When to use:** New accent, adjusted contrast, or a token needed by multiple modules.

## Checklist

1. Decide scope:
   - **Both modes** → define in `src/tokens.css` under `body` (e.g. `--idunn-*`)
   - **One mode only** → set the Obsidian variable in `src/dark.css` or `src/light.css`
2. Prefer mapping Obsidian vars to Idunn tokens:

   ```css
   body {
     --idunn-new-accent: #2aa8c4;
     --text-accent: var(--idunn-new-accent);
   }
   ```

3. If the token is mode-specific, override in `.theme-dark` / `.theme-light` only.
4. Update [../reference/design-tokens.md](../reference/design-tokens.md) with the new name and hex.
5. Run `npm run build`.
6. Check Dark and Light in Obsidian (headings, links, buttons as relevant).

## Do / don’t

| Do | Don’t |
|----|--------|
| Use Obsidian’s published CSS variables | Hard-code colors on many selectors |
| Keep `--idunn-*` as the brand source of truth | Duplicate the same hex in dark + light without reason |
| Rebuild `theme.css` before committing | Edit only `theme.css` by hand |

## Related

- [tune-syntax-highlighting.md](tune-syntax-highlighting.md)
- [../reference/css-variable-map.md](../reference/css-variable-map.md)
