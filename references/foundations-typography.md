# Typography foundations

## Family

- `JetBrains Mono` at weights 400 and 600 as the primary and UI family.
- `IBM Plex Mono` only as a fallback for small technical glyphs.
- Fall back to `ui-monospace`, `SFMono-Regular`, then `monospace`.

## Roles

| Token | Size / line height | Weight | Tracking | Use |
| --- | --- | --- | --- | --- |
| `type.display` | `clamp(2.125rem, 6vw, 5.75rem) / .98` | 600 | `-.07em` | Large editorial or blueprint statement |
| `type.heading` | `clamp(1.375rem, 3vw, 2.375rem) / 1.1` | 600 | `-.045em` | Section heading |
| `type.body` | `1.125rem / 1.6` | 400 | normal | Primary website copy |
| `type.ui` | `1rem / 1.4` | 400 or 600 | normal | Inputs, selectors, actions, and short labels |
| `type.meta` | `.75rem–.875rem / 1.4` | 400 | normal or `.09em` uppercase | Metadata and system annotations |

## Usage rules

- Use weight 600 sparingly for headings, selected keys, and ASCII artwork.
- Use `color.text.muted` for metadata and supporting copy.
- Keep body line length near 45–75 characters when possible.
- Preserve spaces and line breaks.
- Do not use tight negative tracking below heading sizes.
- Do not use uppercase.

## CSS source mapping

```css
@import url("https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600&display=swap");

:root {
  --font-mono: "JetBrains Mono", ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
}

body {
  font-family: var(--font-mono);
  font-size: 18px;
  line-height: 1.6;
}
```
