# Action elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

| Element | Purpose | Required anatomy |
| --- | --- | --- |
| Button | Trigger an immediate operation | Label; optional leading or trailing icon |
| Icon button | Trigger a compact operation | Icon; accessible name; optional tooltip |
| Text action | Offer a quiet standalone operation | Short verb label |
| Link | Navigate to a destination | Descriptive text; destination semantics |

## Anatomy

| Element | Minimum block size | Padding | Internal gap | Radius |
| --- | --- | --- | --- | --- |
| Button | `space.10` | `space.2` block, `space.3` inline | `space.2` | `radius.1` |
| Small button | `2 × space.4` | `space.1` block, `space.2` inline | `space.1` | `radius.1` |
| Icon button | `space.10` square target | `space.2` | — | `radius.1` |
| Text action | Content-sized | `space.1` block | `space.1` | `radius.1` when focused |
| Inline link | Content-sized | None | `space.1` to an adjacent icon | None |

Keep icons at `1em` so they scale with the action label. Center content on both axes and do not compress the minimum target to match a small glyph.

## Variants

- Primary: the single strongest action in a region; use `color.action.primary`.
- Secondary: default action when emphasis is moderate.
- Ghost: low-emphasis action without a persistent container.
- Danger: destructive or difficult-to-reverse action; use `color.status.danger`.
- Small: compact toolbar or dense-row action; keep the target operable.

## States

Define rest, hover, focus-visible, active, disabled, and loading states. Preserve the label width while loading. A disabled action must look inactive and be programmatically unavailable; do not use it to explain why an action cannot run.

## Behavior

- Use a button for an operation and a link for navigation.
- Keep one primary action per local decision area.
- Do not trigger an action on pointer-down; allow cancellation before activation.
- Use the pointer cursor asset for actionable regions.
- Keep icon-only actions visually compact while preserving an adequate hit target.

## Content

- Start labels with a specific verb: Save, Upload, Retry, or Delete.
- Keep labels stable between rest and loading states.
- Avoid generic labels such as “OK” when the outcome can be named.