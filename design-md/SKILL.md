---
name: design-md
description: "Analyze any web project's codebase and synthesize a semantic design system into DESIGN.md files"
source: "Modified from https://github.com/google-labs-code/stitch-skills/tree/main/skills/design-md"
risk: safe
---

# DESIGN.md Skill

You are an expert Design Systems Lead. Your goal is to analyze the project's existing codebase, stylesheets, components, and UI patterns, then synthesize a comprehensive "Semantic Design System" into a file named `DESIGN.md`.

## When to Use This Skill

Use this skill when:
- Analyzing any web or mobile project's design system
- Creating DESIGN.md files for existing codebases
- Synthesizing semantic design systems from source code
- Documenting UI/UX patterns, tokens, and conventions for AI agent handoff
- Generating design documentation so other developers or AI agents can maintain visual consistency

## Overview

This skill helps you create `DESIGN.md` files that serve as the "source of truth" for a project's visual design language. By analyzing the actual codebase — CSS files, Tailwind config, component libraries, theme files, design tokens, and rendered UI — you produce a human-readable and AI-readable document that captures the complete design system. This ensures that anyone (human or AI) working on the project can maintain visual consistency without guessing.

## Prerequisites

- Access to the project's source code (local filesystem)
- A project with existing UI components or screens (at least one rendered page or component)

## The Goal

The `DESIGN.md` file will serve as the "source of truth" for the project's visual design language. It captures the design system in descriptive, semantic terms backed by precise technical values, so that any developer or AI agent can:
1. Understand the visual identity at a glance
2. Create new components that match the existing design
3. Make informed decisions about UI changes without breaking consistency

## Analysis & Discovery Process

To analyze a project's design system, follow these steps:

### Step 1: Locate Design-Related Files
Scan the project for design-relevant files and configurations:
- **CSS/SCSS/LESS files** — Global styles, variables, custom properties
- **Tailwind config** — `tailwind.config.js/ts` for theme extensions, colors, fonts, spacing
- **Theme files** — Any `theme.js/ts`, `tokens.js/ts`, `variables.css`, or design token files
- **Component library** — Shared UI components (buttons, cards, inputs, modals, etc.)
- **Layout files** — Root layouts, page templates, navigation structures
- **Package.json** — UI libraries in use (e.g., shadcn/ui, Material UI, Chakra, Radix, Ant Design)
- **Global styles** — `globals.css`, `app.css`, `index.css`, or equivalent entry stylesheets
- **Figma/design references** — Any linked design files or screenshots in the repo

### Step 2: Extract Design Tokens
From the files discovered above, extract:
- **Colors** — Primary, secondary, accent, background, foreground, muted, destructive, border, etc.
- **Typography** — Font families, sizes, weights, line heights, letter spacing
- **Spacing** — Padding/margin scales, gap values, container widths
- **Border radius** — Corner rounding values across components
- **Shadows** — Box shadow definitions and elevation levels
- **Breakpoints** — Responsive design breakpoints
- **Animations/Transitions** — Duration, easing, and motion patterns
- **Z-index scale** — Layering strategy

### Step 3: Analyze Component Patterns
Review the actual UI components to understand:
- How buttons are styled (variants, sizes, states)
- How cards/containers are structured (padding, borders, shadows)
- How forms and inputs are designed (borders, focus states, error states)
- How navigation works (layout, active states, mobile behavior)
- How modals/dialogs are presented (overlay, animation, sizing)
- How data tables are styled (headers, rows, hover states)
- How feedback elements work (toasts, alerts, badges)

### Step 4: Capture the Visual Atmosphere
Look at the overall rendered UI (or screenshots if available) and describe:
- The overall mood and aesthetic philosophy
- Light/dark mode support and implementation
- Visual density (spacious vs. compact)
- Design style (minimalist, glassmorphism, brutalist, skeuomorphic, flat, etc.)

## Analysis & Synthesis Instructions

### 1. Extract Project Identity
- Locate the Project Title (from package.json, README, or root layout)
- Identify the tech stack (React, Vue, Svelte, Next.js, etc.)
- Identify the CSS approach (Tailwind, CSS Modules, styled-components, vanilla CSS, etc.)
- Identify any UI component library in use

### 2. Define the Atmosphere
Evaluate the UI to capture the overall "vibe." Use evocative adjectives to describe the mood (e.g., "Airy," "Dense," "Minimalist," "Utilitarian," "Playful," "Corporate," "Warm," "Clinical").

### 3. Map the Color Palette
Identify the key colors in the system. For each color, provide:
- A descriptive, natural language name that conveys its character (e.g., "Deep Muted Teal-Navy")
- The specific hex/HSL/RGB code in parentheses for precision (e.g., "#294056" or "hsl(210, 40%, 98%)")
- Its CSS variable name if applicable (e.g., `--primary`, `--background`)
- Its specific functional role (e.g., "Used for primary action buttons and links")

### 4. Document Typography
For each typographic level, describe:
- Font family and fallback stack
- Weight usage for headings vs. body vs. UI elements
- Size scale and how it maps to semantic usage (h1, h2, body, caption, etc.)
- Letter-spacing and line-height character
- Any special typographic treatments (gradients, shadows, truncation)

### 5. Translate Geometry & Shape
Convert technical border-radius and layout values into physical descriptions:
- Describe `rounded-full` as "Pill-shaped"
- Describe `rounded-lg` / `12px` as "Generously rounded corners"
- Describe `rounded-md` / `6px` as "Subtly rounded corners"
- Describe `rounded-none` / `0px` as "Sharp, squared-off edges"
- Document the dominant shape language of the project

### 6. Describe Depth & Elevation
Explain how the UI handles layers:
- Describe the presence and quality of shadows (e.g., "Flat," "Whisper-soft diffused shadows," "Heavy, high-contrast drop shadows")
- Document the elevation scale (how many levels, what each is used for)
- Note any glassmorphism, blur effects, or overlay treatments

### 7. Document Spacing & Layout
- Grid system (12-column, flexbox-based, CSS Grid, etc.)
- Container max-widths and padding
- Consistent spacing scale and how it's applied
- Responsive behavior and breakpoint strategy

### 8. Capture Interaction Patterns
- Hover states (color shifts, scale, shadow changes)
- Focus indicators (outline style, ring color)
- Active/pressed states
- Transition durations and easing curves
- Loading states and skeleton patterns

## Output Guidelines

- **Language:** Use descriptive design terminology and natural language, backed by precise technical values
- **Format:** Generate a clean Markdown file following the structure below
- **Precision:** Include exact values (hex codes, pixel values, CSS variables) alongside descriptive names
- **Context:** Explain the "why" behind design decisions, not just the "what"
- **AI-Readable:** Structure the document so an AI agent can parse it and apply the design system programmatically

## Output Format (DESIGN.md Structure)

```markdown
# Design System: [Project Title]

**Tech Stack:** [e.g., Next.js + Tailwind CSS + shadcn/ui]
**CSS Approach:** [e.g., Tailwind utility-first with CSS custom properties]
**Last Updated:** [Date]

## 1. Visual Theme & Atmosphere
(Description of the mood, density, aesthetic philosophy, and design style.)
(Light/dark mode support and implementation details.)

## 2. Color Palette & Roles

### Core Colors
| Role | Name | Value | CSS Variable | Usage |
|------|------|-------|-------------|-------|
| Primary | ... | ... | ... | ... |
| Secondary | ... | ... | ... | ... |
| ... | ... | ... | ... | ... |

### Semantic Colors
(Success, warning, error, info colors with their values and usage.)

### Dark Mode Adjustments
(How colors shift in dark mode, if applicable.)

## 3. Typography System

### Font Stack
(Primary and secondary font families with fallbacks.)

### Type Scale
| Level | Size | Weight | Line Height | Usage |
|-------|------|--------|-------------|-------|
| H1 | ... | ... | ... | ... |
| Body | ... | ... | ... | ... |
| ... | ... | ... | ... | ... |

## 4. Spacing & Layout

### Spacing Scale
(Base unit and scale: 4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px, etc.)

### Grid & Container
(Max-width, padding, column system, responsive behavior.)

### Breakpoints
| Name | Value | Behavior |
|------|-------|----------|
| sm | ... | ... |
| md | ... | ... |
| ... | ... | ... |

## 5. Component Stylings

### Buttons
(Shape, color variants, sizes, hover/active/disabled states.)

### Cards & Containers
(Corner roundness, background, border, shadow, padding.)

### Inputs & Forms
(Border style, focus ring, error states, label positioning.)

### Navigation
(Layout pattern, active indicators, mobile behavior.)

### Modals & Dialogs
(Overlay style, animation, sizing, close behavior.)

### Data Display
(Tables, lists, badges, tags — styling patterns.)

## 6. Depth & Elevation
(Shadow scale, layering strategy, z-index conventions.)

## 7. Motion & Animation
(Transition durations, easing curves, animation patterns.)

## 8. Iconography & Assets
(Icon library in use, icon sizing, illustration style.)

## 9. Accessibility Notes
(Color contrast ratios, focus indicators, ARIA patterns observed.)

## 10. Design Conventions & Rules
(Any unwritten rules observed in the codebase — naming conventions, component composition patterns, responsive strategies.)
```

## Usage Example

To use this skill for any web project:

1. **Scan the project structure:**
   ```
   Identify all CSS, theme, config, and component files in the project
   ```

2. **Read the configuration files:**
   ```
   Parse tailwind.config.js, theme files, CSS variables, package.json
   ```

3. **Analyze key components:**
   ```
   Read button, card, input, layout, and navigation components
   ```

4. **Review rendered output (if available):**
   ```
   Check screenshots, Storybook, or run the dev server to see the actual UI
   ```

5. **Synthesize and generate:**
   - Create `DESIGN.md` in the project root directory
   - Follow the prescribed format exactly
   - Ensure all color codes and values are accurate
   - Use evocative, designer-friendly language alongside precise values

## Best Practices

- **Be Descriptive:** Avoid generic terms like "blue" or "rounded." Use "Ocean-deep Cerulean (#0077B6)" or "Gently curved edges (8px)"
- **Be Functional:** Always explain what each design element is used for
- **Be Consistent:** Use the same terminology throughout the document
- **Be Visual:** Help readers visualize the design through your descriptions
- **Be Precise:** Include exact values (hex codes, pixel values, CSS variables) in parentheses after natural language descriptions
- **Be Complete:** Cover all aspects of the design system, even subtle ones like transition timing
- **Be Practical:** Include enough detail that an AI agent could recreate the design system from this document alone

## Tips for Success

1. **Start with the config files:** `tailwind.config.js`, `theme.js`, or CSS variables give you the foundation
2. **Look for patterns:** Identify consistent spacing, sizing, and styling patterns across components
3. **Think semantically:** Name colors by their purpose, not just their appearance
4. **Consider hierarchy:** Document how visual weight and importance are communicated
5. **Check for dark mode:** Many modern projects have dual themes — document both
6. **Read the component library:** If using shadcn/ui, Material UI, etc., note which components are customized and how
7. **Note deviations:** If some components break the pattern, document those exceptions too

## Common Pitfalls to Avoid

- Using technical jargon without translation (e.g., "rounded-xl" instead of "generously rounded corners")
- Omitting color codes or using only descriptive names
- Forgetting to explain functional roles of design elements
- Being too vague in atmosphere descriptions
- Ignoring subtle design details like shadows or spacing patterns
- Missing dark mode or responsive variations
- Not documenting the CSS approach (Tailwind vs. CSS Modules vs. styled-components)
- Forgetting interaction states (hover, focus, active, disabled)
