# Design System Skill

A modular skill for creating, evaluating, and modifying visual interfaces without loading an entire design system into context at once.

The skill separates stable foundations from reusable interface elements. AI agent loads only the references needed for the current design task while preserving the patterns already established inside the target project.

## Idea behind 

DESIGN.md can be too broad or too narrow. And it allows no context control, you always load everything at once. Another problem is consistency in bigger teams including non-designers. DESIGN.md leaves a wider variation and thus develops lack of consistency across team. 

From the other side introducing complete design system built for example in Figma is always overkill when we are speaking about quick prototyping, graphical art work, or unusual formats.

This is why I came up with the idea of finding a middle ground between them. That will be easy to maintain in a team, since skills can be easily shared. 

Here you see the example of my personal skill, that I use in my multi-agent setup (Hermes, Codex, Claude) that generates such output formats:
- PDF files
- Websites
- Desktop Apps
- Web Apps
- Mobile Interfaces
- Visuals for articles
- Walkthrough Video-animations


## Structure

```text
design-system/
├── SKILL.md
├── assets/
│   ├── cursor-default.svg
│   ├── cursor-pointer.svg
│   └── cursor-text.svg
└── references/
    ├── foundations-colors.md
    ├── foundations-layout.md
    ├── foundations-typography.md
    ├── foundations-visuals.md
    ├── elements-actions.md
    ├── elements-feedback.md
    ├── elements-fields.md
    ├── elements-files.md
    ├── elements-navigation.md
    ├── elements-overlays.md
    ├── elements-status.md
    └── elements-surfaces.md
```

## How it works

The skill uses progressive disclosure:

1. `SKILL.md` routes the request to the appropriate design layer.
2. Foundation references provide shared colors, typography, layout, and visual language.
3. Element references define anatomy, variants, states, behavior, accessibility, and foundation dependencies.
4. Existing project components and tokens take priority over the general guidance in this skill.

This structure keeps shared values centralized. A color, spacing value, or typography rule can be updated in its foundation reference without repeating the change across every element.

## Install

Please do not install this skill. tbh it makes no sense since it is a personal skill.
You can navigate your agent to this repo, and ask it to help you to build your own design-skill using mine as an example.

