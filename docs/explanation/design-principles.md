# Explanation: design principles

**Scope:** Why Idunn looks the way it does — intent behind palette and contrast choices.  
**When to use:** Deciding whether a visual change fits the theme; onboarding contributors or agents.

## Name and mood

Idunn evokes spring and renewal: cool water (ocean / cyan) with living green (emerald). The UI should feel calm and clear, not neon or playful.

## Audience

Optimized for **developers and technical documentation** in Obsidian:

- Long reading sessions → soft surfaces, restrained chrome
- Code-heavy notes → high-contrast syntax, especially C++ and Markdown
- Dual workflows → first-class Dark and Light, not an afterthought light invert

## Color roles

| Role | Hue family | Typical use |
|------|------------|-------------|
| Primary accent | Cyan | Links, active tab cue, `--text-accent` |
| Depth | Ocean blue | Secondary accents, external links, light-mode emphasis |
| Action / growth | Emerald | Interactive accent, tags, blockquote edge, success |

Headings step through cyan → emerald so outline structure is scannable without shouting.

## CSS strategy

- Override Obsidian’s CSS variables; minimize bespoke selectors.
- Keep brand hex in `--idunn-*` so accents stay consistent.
- Rebuild from `src/` so `theme.css` stays a reproducible artifact.

## Non-goals (for now)

- Heavy animation or decorative flourishes
- Mimicking a specific IDE skin 1:1
- Per-plugin restyles unless they break core readability
