# GUI Workflow Design Checklist

Use this checklist when designing the interface flow for a new feature to ensure a seamless User Experience (UX).

## 1. Task Mapping & Flow
- [ ] **Job to be Done (JTBD):** Is the core user goal clearly defined?
- [ ] **Happy Path:** Is the primary route to success mapped out with minimal friction?
- [ ] **Edge Cases:** Are alternative flows (e.g., empty states, error states, timeouts) mapped out?
- [ ] **The 3-Click Rule:** Can the user reach their core objective within 3 clicks from the entry point?

## 2. Information Architecture (IA)
- [ ] **Logical Grouping:** Are related functions grouped together intuitively?
- [ ] **Visual Hierarchy:** Does the size, color, and placement of elements reflect their importance?
- [ ] **Progressive Disclosure:** Are advanced/secondary options hidden until needed to prevent cognitive overload?

## 3. Interaction & Feedback
- [ ] **Affordance:** Do interactive elements look clickable/editable?
- [ ] **Feedback Loops:** Does every action have a visible system response? (e.g., loading spinners, success toasts, error alerts).
- [ ] **Error Prevention:** Are destructive actions guarded (e.g., confirmation dialogs)? Are form submission buttons disabled until the form is valid?

## 4. Consistency
- [ ] **Design System:** Does the flow adhere to established UI patterns (e.g., Fluent 2 guidelines, consistent color theory: Red=Error, Green=Success)?
- [ ] **Recognition over Recall:** Is necessary context kept visible so the user doesn't have to memorize information from previous steps?
