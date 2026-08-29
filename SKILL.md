---
name: design-system
description: use whenever the user asks to create, evaluate, or modify a visual interface or graphical design, and there is no needed element or examples inside of the project.
---

# Design System

Use the smallest reference set that can answer the request. Do not load every foundation file by default.

## Route the request

1. First use elements and foundation inside of project that you are working on.
2. Design-system is a guideline, for initiation of new elements and tokens.
3. Identify the requested layer: foundation or element.
4. Load only the matching references and their direct dependencies.
5. Use elements guides for child elements (example: card with checkbox - use elements-fields.md and elements-surfaces.md for it)
6. Keep product-specific workflows and page arrangements outside this skill.
7. Load multiple files only when the output crosses those concerns.

## Foundation references

- [references/foundations-colors.md] Use this file for color primitives, semantic roles, interaction states, and color constraints.
- [references/foundations-typography.md] Use this file for font selection, type roles, hierarchy, spacing, and text behavior.
- [references/foundations-visuals.md] Use this file for ASCII artwork, cursor treatments, pixel-style imagery, decorative gradients, and reusable visual assets.
- [references/foundations-layout.md] Use this file for spacing, responsive structure, sizing, borders, radii, elevation, and layout behavior.

## Element references

- [references/elements-actions.md] Use this file for buttons, icon buttons, text actions, links.
- [references/elements-fields.md] Use this file for inputs, textareas, selects, choices, range controls, labels, validation, checkboxes.
- [references/elements-navigation.md] Use this file for tabs, selectable rows, menu items, disclosure controls.
- [references/elements-status.md] Use this file for badges, tags, pills, counts, status indicators, and compact progress.
- [references/elements-feedback.md] Use this file for notices, toasts, empty states, loading indicators, skeletons, and errors.
- [references/elements-surfaces.md] Use this file for cards, panels, data rows, statistics, code regions, dividers, and scroll containers.
- [references/elements-overlays.md] Use this file for menus, dropdowns, tooltips, popovers, dialogs, drawers, and focus management.
- [references/elements-files.md] Use this file for file pickers, upload rows, media tiles, drop zones, selection, and removal states.

## Work with elements

Treat elements as context-independent interface units. Include their anatomy, variants, states, behavior, accessibility, and foundation dependencies.

## Source priority

1. Examples, components, tokens, elements, UIs inside of current project
2. User inputs/prompts
2. Foundation references
3. Element references
