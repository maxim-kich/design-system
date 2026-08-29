# Status elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

- Badge or tag for categorical metadata.
- Chip for a compact value that may be removable or selectable.
- Pill for a short state label.
- Count for collection quantity.
- Status dot for a secondary visual cue.
- Compact progress indicator for bounded or ongoing work.

## Anatomy

| Element | Padding or size | Internal gap | Shape |
| --- | --- | --- | --- |
| Badge or tag | `space.1` block, `space.2` inline | `space.1` | `radius.1` |
| Chip | `space.1` block, `space.2` inline | `space.1` | `radius.full` |
| Status pill | `space.1` block, `space.2` inline | `space.1` | `radius.full` |
| Count | `space.1` minimum inline padding | — | `radius.full` when contained |
| Status dot | `space.2` square | `space.2` to its label | `radius.full` |
| Compact progress | `space.1` track thickness | `space.2` to its label | `radius.full` |

Keep labels on one line when practical. A removable chip includes an end-aligned remove action with its own accessible name.

## Semantic roles

| Role | Token | Examples |
| --- | --- | --- |
| Neutral | `color.status.neutral` | Waiting, inactive, unavailable |
| Success | `color.status.success` | Connected, current, running, successful |
| Warning | `color.status.warning` | Needs attention or authentication |
| Info | `color.status.info` | Informational, stale, or completed |
| Danger | `color.status.danger` | Failed, missing, or destructive |

## Rules

- Pair status color with a written label, icon, pattern, or shape.
- Use the semantic role that describes meaning, not the visually closest hue.
- Keep status labels short, stable, and sentence case.
- Use a count only when the quantity helps the next decision.
- Reserve animated progress for work that is actually ongoing.
- Do not make a decorative badge interactive; use a button or link when activation is required.
- Keep removable chips distinct from static tags and provide a named remove action.
