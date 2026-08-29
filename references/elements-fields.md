# Field elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

| Element | Purpose | Required anatomy |
| --- | --- | --- |
| Text input | Enter or edit a single line | Label; control; optional hint, prefix, suffix, or error |
| Textarea | Enter or edit multiple lines | Label; resizable control; optional hint, count, or error |
| Select | Choose one option from a longer set | Label; selected value; indicator; option list |
| Checkbox | Make an independent yes/no selection | Marker; label; optional description |
| Toggle | Change a setting that takes effect immediately | Track; thumb; label; optional status |
| Radio or card choice | Choose one option from a visible set | Marker; label; optional description |
| Range | Choose a value on a bounded scale | Label; track; thumb; current value |
| File picker | Select one or more local files | Visible trigger; native file input; selection note |

## Anatomy

| Element or region | Minimum size | Padding | Internal gap | Radius |
| --- | --- | --- | --- | --- |
| Field stack | Content-sized | None | `space.2` | None |
| Label row | Content-sized | None | `space.1` | None |
| Text input or select | `space.10` block | `space.2` block, `space.3` inline | `space.2` | `radius.1` |
| Textarea | `3 × space.10` initial block | `space.2` block, `space.3` inline | `space.2` | `radius.1` |
| Checkbox | `space.10` target; `space.4` marker; `space.1 × space.2` check | None | `space.2` | `radius.1` |
| Radio | `space.10` target; `space.4` marker; `space.2` inner dot | None | `space.2` | `radius.full` |
| Toggle | `space.10` inline, `space.6` block | `space.1` | `space.2` to label | `radius.full` |
| Choice card | `space.10` block | `space.3` | `space.2` | `radius.1` |
| Range | `space.10` block target; `space.1` track; `space.4` thumb | None | `space.2` to value | `radius.full` |
| Field group | Content-sized | None | `space.4` | None |

Keep the label, control, hint, and validation message in one field stack. Align prefixes and suffixes inside the control without reducing the editable region below a useful width. Draw the checkbox check with `border.width.default` end and bottom strokes rotated 45 degrees; do not use a font glyph.

## Variants

- Standard: persistent label above a full-width control.
- Compact: shorter labels and metadata, but the same operable target size.
- Affixed: leading prefix or trailing unit, indicator, or action.
- Inline choice: checkbox, radio, or toggle beside its label.
- Choice card: radio behavior with supporting text inside a larger target.
- File trigger: button-like label backed by a native file input.

## States

Define empty, populated, hover, focus-visible, invalid, disabled, read-only, and loading states where applicable. Use `color.bg.interactive` for clear hover feedback, `color.action.primary` for focus or selection, and `color.status.danger` with a written message for invalid input. Read-only content remains selectable; disabled content does not.

## Behavior

- Prefer native controls when their behavior meets the need.
- Keep labels visible after entry; placeholders are examples, not labels.
- Validate after a meaningful interaction, not before the user begins.
- Preserve entered values and valid selections after a validation error.
- Allow textarea resizing unless it would break a constrained layout.
- Keep the current range value visible near the control.
- Make the complete label area activate a checkbox, toggle, radio, or card choice.
- Apply a toggle immediately; use a checkbox when confirmation happens later.
- Keep one radio selected in a required group and allow arrow-key movement within it.
- Use a visible button-like label to activate a visually hidden native file input.
- Associate labels, hints, and validation messages with their controls.

## Content

- Use short noun labels that describe the requested value.
- Mark required or optional status consistently; do not rely on an asterisk alone.
- Write placeholders as realistic examples without repeating the label.
- Put format or constraint guidance in the hint before an error occurs.
- State errors specifically and explain how to recover.
- Keep option labels mutually exclusive and parallel in grammar.
