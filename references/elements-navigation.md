# Navigation elements

## Foundation dependencies

- `foundations-colors.md`
- `foundations-typography.md`
- `foundations-layout.md`

## Families

| Element | Purpose |
| --- | --- |
| Tabs | Switch between peer views within one context |
| Selectable row | Open or select an item from a collection |
| Menu item | Choose an action or destination from a temporary list |
| Disclosure trigger | Expand or collapse related content |
| Close control | Dismiss a temporary region |

## Anatomy

| Element | Padding | Internal gap | Minimum size | Shape |
| --- | --- | --- | --- | --- |
| Tab | `space.2` block, `space.3` inline | `space.2` | `space.10` block | `radius.1` when contained |
| Selectable row | `space.3` block, `space.4` inline | `space.3` | Content-led | Default radius or `radius.1` when bounded |
| Menu item | `space.2` block, `space.3` inline | `space.2` | `space.10` block | `radius.1` |
| Disclosure trigger | `space.3` block, `space.4` inline | `space.2` | `space.10` block | Match owning surface |
| Close control | `space.10` square target | `space.2` | `space.10` square | `radius.1` |

Keep a primary label, optional supporting text, and optional status or count. Align secondary metadata to the end without shrinking the primary label below a readable width.

## States

Define rest, hover, focus-visible, active/current, attention, disabled, and nested states only when relevant. Use `color.bg.interactive` for clear hovered or selected feedback and `color.action.primary` for the active cue.

## Behavior

- Preserve the user’s place when switching peer views.
- Use links for destinations and buttons for local view changes.
- Keep only one tab in a set selected.
- Let a selectable row have one primary activation target; separate secondary actions clearly.
- Place menus next to their trigger and return focus to the trigger on dismissal.
- Update `aria-expanded` on disclosure controls.
- Keep the disclosure caret and expanded content synchronized.
- Make close controls available by pointer and keyboard.

## Keyboard

- Tabs: use arrow keys within the tab list and expose the selected tab.
- Menus: support arrow navigation, Home, End, Enter, and Escape when implementing a custom menu.
- Disclosure: activate with Enter or Space.
- Selectable rows: use native links or buttons whenever possible.