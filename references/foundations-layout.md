# Layout foundations

## Principles

- Use a small spacing scale and repeat it consistently.
- Create hierarchy with spacing and surface changes before adding decoration.
- Keep primary content full-width and fluid unless reading comfort requires a maximum width.
- Let content determine height. Reserve fixed heights for controls or viewports.

## Spacing scale

| Token | Value | Typical use |
| --- | --- | --- |
| `space.1` | `4px` | Tight internal separation, compact option gaps |
| `space.2` | `8px` | Default vertical rhythm and compact groups |
| `space.3` | `12px` | Row padding, text-to-control spacing |
| `space.4` | `16px` | Default element gap and compact page gutter |
| `space.6` | `24px` | Section separation and page top offset |
| `space.10` | `40px` | Wide-screen page gutter |

## Responsive structure

| Token | Value | Use |
| --- | --- | --- |
| `breakpoint.compact` | `767px` | Switch from wide to compact behavior |
| `layout.gutter.wide` | `40px` | Wide-screen inline page gutter |
| `layout.gutter.compact` | `16px` | Compact inline end gutter |
| `layout.row.gap.wide` | `16px` | Wide row gap |
| `layout.row.gap.compact` | `8px` | Compact row gap |
| `layout.row.padding-block` | `12px` | Default row padding |

At compact widths, prefer one column. Do not scale the wide layout down.

## Shape and borders

| Token | Value | Use |
| --- | --- | --- |
| `radius.1` | `4px` | Compact options and small interactive states |
| `radius.full` | `999px` | Pills, circular indicators, and fully rounded controls |
| `border.width.default` | `1px` | Standard separation |
| `border.color.default` | `color.text.muted` at reduced opacity | Quiet boundary |

Use a radius only when interaction needs a visible boundary. Default radius is 0px.

## Elevation

| Token | Value | Use |
| --- | --- | --- |
| `elevation.floating` | `0 10px 30px rgba(0, 0, 0, .35)` | Tooltip, menu, or floating preview |
| `elevation.overlay` | `0 20px 60px rgba(0, 0, 0, .32)` | Large elevated region |

Prefer border and surface contrast for ordinary hierarchy. Apply elevation only when a surface floats above content.

## Overflow and text resilience

- Allow prose to wrap naturally.
- Make scroll ownership explicit; avoid nested scrolling unless each region has a distinct purpose.
- Keep media fluid with `max-width: 100%` and intrinsic aspect ratio.

## CSS source mapping

```css
:root {
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-6: 24px;
  --space-10: 40px;
  --radius-1: 4px;
  --radius-full: 999px;
}

.row {
  display: flex;
  gap: var(--space-4);
  padding: var(--space-3) var(--space-10);
}

@media (max-width: 767px) {
  .row {
    gap: var(--space-2);
    padding-inline: 0 var(--space-4);
  }
}
```
