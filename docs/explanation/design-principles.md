# Explanation: design principles

**Scope:** Why Idunn looks the way it does — intent behind palette and contrast choices.  
**When to use:** Deciding whether a visual change fits the theme; onboarding contributors or agents.

## Name and mood

Idunn evokes spring and renewal: living teal (growth) with clear blues (focus and calm water). The UI should feel calm and clear, not neon or playful.

## Audience

Optimized for **developers and technical documentation** in Obsidian:

- Long reading sessions → soft surfaces, restrained chrome
- Code-heavy notes → high-contrast syntax, especially C++ and Markdown
- Dual workflows → first-class Dark and Light, not an afterthought light invert

## Color roles

| Role | Hue family | Typical use |
|------|------------|-------------|
| Brand / growth | Teal (`--idunn-emerald`) | H2, tags, blockquote edge, success |
| Links | Soft blue (`--idunn-cyan`) | Links, tab cue, `--text-accent` |
| Action / depth | Deeper blue (`--idunn-ocean`) | Interactive accent, H4, external emphasis |

Headings: calm H1 (body text), teal H2, blue H3/H4 — scannable without shouting.

## CSS strategy

- Override Obsidian’s CSS variables; minimize bespoke selectors.
- Keep brand hex in `--idunn-*` so accents stay consistent.
- Rebuild from `src/` so `theme.css` stays a reproducible artifact.
- Palette experiments belong in `previews/*.html` before changing CSS.

## Non-goals (for now)

- Heavy animation or decorative flourishes
- Per-plugin restyles unless they break core readability
