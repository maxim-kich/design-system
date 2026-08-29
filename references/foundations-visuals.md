# Visual foundations

## ASCII language

- Use ASCII as a meaningful identity element, section marker, portrait treatment, or state illustration.
- Keep ASCII secondary to usable content and interaction.
- Prefer live text when it must scale, animate, or adapt; prefer an SVG asset when exact character alignment is more important.
- Apply `color.visual.gradient-start` to `color.visual.gradient-end` to branded ASCII artwork.
- Scale dense ASCII down only while individual characters remain legible.
- Never stretch ASCII disproportionately.

```css
.ascii-visual {
  color: transparent;
  background: linear-gradient(
    to bottom,
    var(--color-visual-gradient-start),
    var(--color-visual-gradient-end)
  );
  background-clip: text;
  font: 600 0.65rem/1.1 var(--font-mono);
  white-space: pre;
}
```

## Accessibility

- Mark purely decorative ASCII with `aria-hidden="true"`.
- Do not require users to interpret dense character art to complete a task.
- Preserve ordinary pointer and text-cursor fallbacks when custom cursor assets fail.

## Cursor language

- Use the default cursor asset for the general canvas.
- Use the pointer cursor asset for links, buttons, selectors, and other actionable regions.
- Use the text cursor asset for editable or selectable text regions.
- Keep the browser-native cursor as the final fallback.

## Asset inventory

| Asset | Use |
| --- | --- |
| `assets/cursor-default.svg` | Default canvas cursor |
| `assets/cursor-pointer.svg` | Interactive control cursor |
| `assets/cursor-text.svg` | Text and input cursor |

Copy an asset into the output project.
