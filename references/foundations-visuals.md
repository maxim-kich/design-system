# Visual foundations

## ASCII language

- Use ASCII as a meaningful identity element, section marker, portrait treatment, or state illustration.
- Keep ASCII secondary to usable content and interaction.
- Prefer live text when it must scale, animate, or adapt; prefer an SVG asset when exact character alignment is more important.
- Apply `color.visual.gradient-start` to `color.visual.gradient-end` to branded ASCII artwork.
- Scale dense ASCII down only while individual characters remain legible.
- Never stretch ASCII disproportionately.

### ASCII title example

Use block-character lettering for a short, prominent display heading. Keep the
plain-text title as its accessible name and hide the character art itself so it
is not read one symbol at a time.

```html
<h1 class="ascii-visual ascii-title" aria-label="Maxim"><span aria-hidden="true">███╗   ███╗  █████╗  ██╗  ██╗ ██╗ ███╗   ███╗
████╗ ████║ ██╔══██╗ ╚██╗██╔╝ ██║ ████╗ ████║
██╔████╔██║ ███████║  ╚███╔╝  ██║ ██╔████╔██║
██║╚██╔╝██║ ██╔══██║  ██╔██╗  ██║ ██║╚██╔╝██║
██║ ╚═╝ ██║ ██║  ██║ ██╔╝ ██╗ ██║ ██║ ╚═╝ ██║
╚═╝     ╚═╝ ╚═╝  ╚═╝ ╚═╝  ╚═╝ ╚═╝ ╚═╝     ╚═╝</span></h1>
```

For a compound title, split the name, surname, and role into separate blocks so
their scale and wrapping can be controlled independently. Keep live text on
larger screens; when a block no longer fits legibly, swap it for a matching SVG
asset instead of squeezing or distorting the characters.

```css
.ascii-visual {
  color: transparent;
  background: linear-gradient(
    to bottom,
    var(--color-visual-gradient-start),
    var(--color-visual-gradient-end)
  );
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  font: 600 0.65rem/1.1 var(--font-mono);
  white-space: pre;
}

.ascii-title {
  margin: 0;
  display: block;
  font: 600 0.9rem/1.1 var(--font-mono);
  white-space: pre;
}

.ascii-title--subtitle {
  font-size: 0.45em;
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
