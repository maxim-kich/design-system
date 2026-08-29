# Color foundations

## Principles

- Neutral hierarchy through surface steps before borders or shadows.
- Green for links, active states, selection, progress, and accents.
- No pure white or black.
- Reference semantic tokens in elements; keep hex values here.

## Primitives

| Token | Value | Source use |
| --- | --- | --- |
| `neutral.950` | `#111211` | Canvas background |
| `neutral.900` | `#202221` | Message and raised surface |
| `neutral.800` | `#363936` | Hovered or selected surface |
| `neutral.600` | `#6E746D` | Loading gradient start |
| `neutral.500` | `#777D77` | Muted text and metadata |
| `neutral.100` | `#CFDACD` | Primary text and loading gradient end |
| `green.400` | `#42C07E` | Primary interactive accent |
| `green.700` | `#48765E` | Visual gradient start |
| `green.850` | `#274033` | Visual gradient end |
| `red.500` | `#C15F5F` | Failure and destructive feedback |
| `amber.500` | `#D29922` | Warning and attention |
| `blue.500` | `#4493F8` | Informational, stale, and completed state |

## Semantic aliases

| Token | Primitive | Use |
| --- | --- | --- |
| `color.bg.canvas` | `neutral.950` | Page and deepest canvas |
| `color.bg.surface` | `neutral.900` | Rows, panels, and raised regions |
| `color.bg.interactive` | `neutral.800` | Hovered and selected options |
| `color.text.primary` | `neutral.100` | Primary copy and controls |
| `color.text.muted` | `neutral.500` | Metadata, hints, and secondary copy |
| `color.action.primary` | `green.400` | Links, active states, and selection |
| `color.visual.gradient-start` | `green.700` | ASCII and completion gradients |
| `color.visual.gradient-end` | `green.850` | ASCII and completion gradients |
| `color.loading.start` | `neutral.600` | Animated text-loading gradient |
| `color.loading.end` | `neutral.100` | Animated text-loading gradient |
| `color.status.neutral` | `neutral.500` | Waiting, inactive, and non-urgent state |
| `color.status.success` | `green.400` | Connected, current, running, and successful state |
| `color.status.warning` | `amber.500` | Attention and authentication-required state |
| `color.status.info` | `blue.500` | Informational, stale, and completed state |
| `color.status.danger` | `red.500` | Failure glyphs and destructive feedback |

## Usage rules

- Use `color.bg.canvas` as the default page background.
- Use `color.bg.surface` for a user-authored row or discrete panel.
- Use `color.bg.interactive` only for clear hover, focus, or selection feedback.
- Pair `color.action.primary` with compact targets or text.
- Use the green gradient for visual artwork.
- Never communicate status through color alone; pair it with text, an icon, or another visible indicator.
- Introduce a new primitive only when no existing token can express the required role; always mention about it to user.

## Text selection

- Use `color.action.primary` as the selected-text background.
- Use `color.bg.canvas` as the selected-text foreground.
- Apply the same mapping to standard and Firefox text selection.

## CSS source mapping

```css
:root {
  --color-bg-canvas: #111211;
  --color-bg-surface: #202221;
  --color-bg-interactive: #363936;
  --color-text-primary: #CFDACD;
  --color-text-muted: #777D77;
  --color-action-primary: #42C07E;
  --color-visual-gradient-start: #48765E;
  --color-visual-gradient-end: #274033;
  --color-status-neutral: #777D77;
  --color-status-success: #42C07E;
  --color-status-warning: #D29922;
  --color-status-info: #4493F8;
  --color-status-danger: #C15F5F;
}

::selection {
  background: var(--color-action-primary);
  color: var(--color-bg-canvas);
}

::-moz-selection {
  background: var(--color-action-primary);
  color: var(--color-bg-canvas);
}
```

  
