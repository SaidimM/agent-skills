---
name: notion-stylist
description: Mastery of Notion's visual and structural capabilities to create aesthetic, functional, and branded workspaces via the UI and API.
version: 1.0.0
author: Hermes Agent
metadata:
  hermes:
    tags: [Notion, UI-Design, Aesthetic, Dashboard, Layout, Branding]
---

# Notion Stylist

Use this skill when a user wants to "beautify" a Notion page, create a dashboard, or ensure visual consistency across a workspace.

## 1. Advanced Layout Principles

### Multi-Column Layouts
- **The Dashboard Grid**: Use `column_list` and `column` blocks to create sidebars or grid layouts.
- **Visual Grouping**: Wrap related content inside a `callout` block. Use a consistent background color (e.g., all "Gray" or all "Blue") to create distinct "widgets" on the page.
- **Spacing**: Use empty `paragraph` blocks or horizontal `divider` blocks to manage white space. Avoid clutter by using `toggle` blocks for secondary information.

### Visual Branding
- **Icon Strategy**: Stick to one style (e.g., all Notion-native minimalist icons, or all custom flat-design icons).
- **Headers**: Use custom covers (1500x300px) that match the accent colors used in headings and callouts.
- **Color Palettes**: Stick to 1-2 primary accent colors. For a "Minimalist" look, use Gray and Default. For "Corporate", use Blue and Purple.

## 2. Functional Styling

### Progress Bars (Formula Property)
Use this snippet in database formulas to create a visual progress bar:
```javascript
slice("■■■■■■■■■■", 0, round(prop("Progress") * 10)) + slice("□□□□□□□□□□", 0, 10 - round(prop("Progress") * 10)) + " " + format(round(prop("Progress") * 100)) + "%"
```

### Global Navigation
- **Synced Blocks**: Create a "Navbar" or "Sidebar" in a Synced Block. Place links to all major pages inside it. Copy and paste this block to the top/side of every page in the workspace for instant updates across the board.

### Button Workflows
- Use **Button Blocks** for high-frequency actions (e.g., "New Task", "Clock In", "Quick Note") to keep the UI clean and action-oriented.

## 3. Database Aesthetics

### Gallery View
- **Card Preview**: Use "Page Cover" or "Files & media" for a visual-first layout.
- **Card Size**: Small/Medium for information-heavy grids; Large for portfolio-style displays.

### Board View
- **Color Columns**: Toggle "Color columns" in the Board view settings to add distinct visual lanes for status or categories.

### Table Blocks
Tables are great for comparisons but require specific nested structures in the API.
- `table_width`: Number of columns.
- `has_column_header`: Set to `true` for a header row.
- **Rows**: Must be added as children of type `table_row`.

```json
{
  "type": "table",
  "table": {
    "table_width": 2,
    "has_column_header": true,
    "children": [
      {
        "type": "table_row",
        "table_row": {
          "cells": [
            [{"type": "text", "text": {"content": "Goal"}}],
            [{"type": "text", "text": {"content": "Outcome"}}]
          ]
        }
      }
    ]
  }
}
```

## 5. Workflow: Automated Project Journaling
Use this pattern to keep a Notion dashboard updated with your agentic progress:
1. **Harvest**: Use `session_search` with keywords like "decision", "milestone", "deleted", or "fixed" to find yesterday's highlights.
2. **Synthesize**: Group findings into "Context", "Actions", and "Pending Decisions".
3. **Style**: Apply the `notion-stylist` principles (Callout for status, Columns for side-by-side metrics, Table for outcomes).
4. **Push**: Update a "Daily Log" database or a "Project Hub" page.

## 5. Formatting & Constraints
- **NO Checklists**: Never use `to_do` blocks. Use `bulleted_list_item` instead.
- **Rich Text**: Liberally use `annotations` (`bold`, `italic`, `underline`, `color` like `red_background` or `blue`) within text objects to highlight keywords, statuses, and critical insights.

## Verification Checklist
- [ ] Are headings consistent?
- [ ] Is the spacing intentional?
- [ ] Do icons follow a uniform style?
- [ ] Is the most important information visible without scrolling?
- [ ] Are secondary details tucked into toggles?
