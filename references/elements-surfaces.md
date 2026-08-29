# Surface elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

- Card for one bounded object or summary.
- Panel for a grouped interface region.
- Key-value row for compact metadata.
- Statistic for a labeled value.
- Code region for preformatted technical content.
- Divider for subtle separation.
- Scroll container for a bounded overflow region.

## Anatomy

| Element | Outer padding | Internal gap | Boundary |
| --- | --- | --- | --- |
| Card | `space.4` | `space.3` | Default radius; `border.width.default` when needed |
| Panel header | `space.3` block, `space.4` inline | `space.3` | Bottom border when body separation is needed |
| Panel body | `space.4` | `space.4` | Inherit panel boundary |
| Key-value row | `space.2` block, `space.3` inline | `space.3` | Divider between repeated rows |
| Statistic | `space.3` | `space.1` between label and value | Match owning surface |
| Code region | `space.4` | `space.2` | `radius.1`; horizontal overflow allowed |
| Scroll container | Match contained surface | `space.2` from scrollbar edge | Explicit bounded viewport |

Use a clear heading or label, primary content, optional metadata, and optional actions. Let spacing and surface contrast establish hierarchy before adding borders or elevation.

## Variants and states

Define flat, raised, interactive, selected, active-session, dragging, archived, and disabled variants only when the surface’s behavior requires them. Interactive surfaces must have a single clear primary action and visible focus. Use `color.bg.canvas`, `color.bg.surface`, and `color.bg.interactive` according to depth and state.

## Behavior

- Keep ordinary cards and panels content-sized.
- Separate secondary actions from the surface’s primary activation target.
- Preserve reading order when a layout collapses to one column.
- Use elevation only for genuinely floating content.
- Make scroll ownership obvious and avoid nested scrolling.
- Give a scroll container a bounded size only when the surrounding layout requires it.
- Preserve whitespace and horizontal overflow in code regions without forcing the page itself to overflow.
