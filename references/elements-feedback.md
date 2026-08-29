# Feedback elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

| Element | Use |
| --- | --- |
| Inline notice | Feedback tied to a field, section, or operation |
| Toast | Brief page-level confirmation with an optional action |
| Empty state | Explain why content is absent and what can happen next |
| Spinner | Indeterminate wait in a compact region |
| Skeleton | Preserve the expected shape while content loads |
| Loading label | Describe ongoing work in text |
| Error state | Explain failure and offer recovery |

## Anatomy

| Element | Padding or size | Internal gap | Shape |
| --- | --- | --- | --- |
| Inline notice | `space.3` block, `space.4` inline | `space.3` | `radius.1` |
| Toast | `space.3` block, `space.4` inline | `space.3` | `radius.1` |
| Empty state | `space.6` padding | `space.3` between message groups | Match owning surface |
| Spinner | `space.4` square | `space.2` to its label | `radius.full` |
| Skeleton group | Match final content padding | `space.2` between lines | `radius.1` |
| Error state | `space.4` padding | `space.3` between message and recovery | `radius.1` |

Align an icon or spinner with the first line of text. Keep optional actions in a separate end slot so message wrapping does not disturb their target size.

## Behavior

- Place feedback near the action or content that caused it.
- Keep a toast brief; include Undo only when reversal is immediate and reliable.
- Do not use a toast for information required to complete the task.
- Preserve layout while loading to avoid unnecessary movement.
- Prefer a skeleton when the final structure is predictable and a spinner when it is not.
- Replace loading feedback with success, empty, or error feedback when work ends.
- Give recoverable errors a specific next action such as Retry or Edit.
- Preserve user input after failures whenever possible.

## Status mapping

Use `color.status.neutral`, `success`, `warning`, `info`, or `danger` according to meaning. Use `color.loading.start` and `color.loading.end` for the branded loading treatment. Never rely on color alone.
