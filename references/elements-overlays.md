# Overlay elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

| Element | Modality | Typical use |
| --- | --- | --- |
| Menu or dropdown | Non-modal | Short action or selection list |
| Tooltip | Non-modal | Supplemental label or explanation |
| Popover | Non-modal | Compact interactive disclosure |
| Dialog | Modal | Focused decision or form |
| Drawer | Modal or persistent | Extended detail, tool, or session region |

## Anatomy

| Element | Padding | Internal gap | Shape and elevation |
| --- | --- | --- | --- |
| Menu | `space.1` | `space.1` between items | `radius.1`; `elevation.floating` |
| Tooltip | `space.1` block, `space.2` inline | `space.1` | `radius.1`; `elevation.floating` |
| Popover | `space.3` | `space.3` | `radius.1`; `elevation.floating` |
| Dialog header | `space.4` | `space.3` | Top of `elevation.overlay` surface |
| Dialog body | `space.4` | `space.4` | Continue dialog surface |
| Dialog footer | `space.3` block, `space.4` inline | `space.2` between actions | Continue dialog surface |
| Drawer | `space.4` content inset | `space.4` | `elevation.overlay` when floating |

Keep the close control in the header end slot. Separate overlay sections with spacing first and a border only when their boundaries remain unclear.

## Placement and layering

- Anchor non-modal overlays to their trigger and keep them within the viewport.
- Use `elevation.floating` for menus, tooltips, and popovers.
- Use `elevation.overlay` for dialogs and large floating regions.
- Keep one predictable layering order; do not solve collisions with arbitrary values.
- At compact widths, let complex overlays use the available viewport instead of shrinking their contents.

## Behavior

- Open from an explicit trigger and keep trigger state synchronized.
- Close on Escape and intentional outside interaction when dismissal is safe.
- Return focus to the trigger after dismissal unless the workflow moved focus elsewhere.
- Trap focus inside modal dialogs while open.
- Give dialogs a visible title and clear primary and secondary actions.
- Keep destructive confirmation explicit and separated from cancellation.
- If a drawer is resizable, provide limits and preserve a usable size without dragging.
- Do not put essential information only in a tooltip.