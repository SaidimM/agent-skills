---
name: fluent2-wireframe
description: Design desktop application wireframes using Microsoft's Fluent 2 design language. Use when creating UI/UX layouts that require 12-column grids, 4px spacing, specific corner radii, and Segoe UI Variable typography for Windows-native experiences.
---

# Fluent 2 Wireframing

## Principles
Fluent 2 focuses on **cohesion, focus, and natural platform integration**. It is designed to feel native to Windows while scaling across platforms.

## Core System Specifications

### 1. Layout & Grid
- **12-Column Grid:** Standard for desktop. Enables halves, thirds, and fourths.
- **Baseline Grid:** 4px baseline for vertical rhythm and scannability.
- **Margins & Gutters:** Always multiples of 4px (e.g., 16px, 24px).

### 2. Spacing Ramp
Use the **4px Spacing Ramp** for all gaps, padding, and margins:
- 4, 8, 12, 16, 20, 24, 32, 40, 48, 56, 64px.

### 3. Corner Radii
- **None (0px):** Full-bleed navigation/tab bars.
- **Small (2px):** Very small components (<32px).
- **Medium (4px):** **Standard** for buttons, text fields, and list items.
- **Large (8px):** Prominent cards and large buttons.
- **X-Large (12px):** Popovers, flyouts, and dialogs.
- **Circle (50%):** Avatars.

### 4. Typography (Segoe UI Variable)
- **Body:** 14px (Standard).
- **Caption:** 12px.
- **Subtitle:** 18px.
- **Title:** 20px - 28px.
- **Display:** 36px+.
- All text should align to the 4px baseline.

## Workflow: Creating a Wireframe
1. **Define Regions:** Split the 12-column grid into Nav (e.g., 2 cols), Content (8 cols), and Side Pane (2 cols).
2. **Apply Spacing:** Use the 4px ramp to define outer margins and inner gutters.
3. **Place Components:** Use the [components.md](references/components.md) guide for specific element specs.
4. **Elevation:** Determine if using shadows (tokens 2, 8, 16, 64) or native strokes (1px).

## Wireframe Checklist
- [ ] Is it on a 12-column grid?
- [ ] Are all margins/paddings multiples of 4px?
- [ ] Is Segoe UI Variable used?
- [ ] Are corner radii correct (4px for standard elements)?
- [ ] Does the side nav have a 4px selection indicator?
- [ ] Is there clear hierarchy using the type ramp?

## Resources
- **Component Specs:** Detailed dimensions and patterns in [components.md](references/components.md).
