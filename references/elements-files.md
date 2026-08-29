# File elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

- File picker trigger backed by a native file input.
- Upload row for a queued, uploading, completed, or failed file.
- File row for an existing attachment.
- Media tile with preview and selection state.
- File-type badge for compact format recognition.
- Drop zone for pointer-based file intake.

## Anatomy

| Element | Padding or size | Internal gap | Shape |
| --- | --- | --- | --- |
| File picker trigger | Follow small button anatomy | `space.1` | `radius.1` |
| Upload or file row | `space.3` | `space.3` | `radius.1` when bounded |
| Media tile | `space.2` | `space.2` | `radius.1` |
| Preview | Fluid inline size; preserve intrinsic ratio | `space.2` to metadata | `radius.1` |
| File-type badge | Follow status badge anatomy | `space.1` | `radius.1` |
| Drop zone | `space.6` | `space.3` | `radius.1`; visible boundary |
| Remove action | `space.10` square target | `space.2` from filename | `radius.1` |

Show the file name, type or preview, optional size, current state, and contextual actions. Truncate long display names visually while preserving the full name in accessible text or a title. Keep selection and removal controls distinct.

## States

Define empty, drag-ready, drag-active, selected, uploading, complete, invalid, failed, and disabled states as needed. Map feedback through the semantic status tokens and include written state text.

## Behavior

- Use a visible button-like label to activate the native file picker.
- State accepted formats, size limits, and multiplicity before selection.
- Validate type and size before beginning an upload when possible.
- Preserve valid files when one item fails validation.
- Show per-file progress when multiple uploads can finish independently.
- Require a deliberate remove action and make reversal available when practical.
- Treat a drop zone as an additional input method, never the only one.
- Keep media selection separate from opening a preview.