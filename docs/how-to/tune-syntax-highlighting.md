# How to: tune syntax highlighting

**Scope:** Improve readability of code blocks (focus: C++ and Markdown).  
**When to use:** Comments wash out, keywords clash with background, or Live Preview tokens look wrong.

## Where to edit

| Concern | File |
|---------|------|
| Token colors per mode | `src/dark.css` / `src/light.css` (`--code-*`) |
| Shared code chrome (size, radius) | `src/code.css` |
| Editor vs reading-view selectors | `src/code.css` |

## Checklist

1. Open a note with a C++ fence and a Markdown fence in both Reading and Live Preview.
2. Adjust semantic vars first (`--code-keyword`, `--code-string`, `--code-comment`, `--code-function`, `--code-value`, `--code-operator`, `--code-tag`).
3. Keep comment color quieter than keywords; keep strings distinct from types/functions.
4. Verify **Light** mode contrast (light backgrounds need darker string/keyword hues).
5. Run `npm run build` and re-check both modes.

## Quick contrast targets

- Comment vs background: clearly secondary, still readable
- Keyword vs string: different hue families (purple/magenta vs green)
- Function vs property: cyan/ocean vs emerald

## Related

- [add-color-token.md](add-color-token.md)
- [../explanation/design-principles.md](../explanation/design-principles.md)
