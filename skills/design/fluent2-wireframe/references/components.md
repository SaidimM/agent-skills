# Fluent 2 Component Specifications

## Navigation
### Side Navigation (Nav Rail/Pane)
- **Selection Indicator:** A 4px wide, 24px high vertical bar in the primary color, aligned to the left edge of the active item.
- **Hierarchy:** Supports up to 2 levels. Categories and Sub-items.
- **Collapse/Expand:** Triggered by a persistent Hamburger menu icon at the top left.

### Top Navigation Bar
- **Page Title:** Short (1-2 words), left-aligned.
- **Contextual Actions:** Placed on the right (e.g., Edit, Search, More).
- **Back Button:** Standard chevron-left for navigation history.

## Buttons & Inputs
### Buttons
- **Corner Radius:** 4px (Medium) for standard; 8px (Large) for prominent CTA cards.
- **Height:** 32px (Small), 40px (Standard), 48px (Large).
- **Styling:** Primary (solid fill), Secondary (stroke), Ghost (no fill/stroke).

### Text Fields
- **Corner Radius:** 4px (Medium).
- **Visual:** Single 1px bottom stroke in focused state, or full stroke outline for high-density forms.
- **Label:** Small caption text above the field (4px gap).

## Selection & Feedback
### Segmented Control
- Used for quick view switching.
- Pill-shaped or rounded-rect (4px) background for the active segment.

### Progress Indicators
- **Linear:** 4px height.
- **Circular:** 24px or 32px diameter.

## Layering & Elevation
### Elevation Tokens (Blur values)
- **Shadow 2:** Low elevation (e.g., buttons on hover).
- **Shadow 8:** Standard elevation (e.g., cards).
- **Shadow 16:** High elevation (e.g., flyouts, dropdowns).
- **Shadow 64:** Modal elevation (e.g., dialogs).

### Strokes (Windows Native)
- Use a 1px solid stroke instead of shadows for a cleaner "native" look on Windows.
