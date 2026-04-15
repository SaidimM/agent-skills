---
name: saas-wireframe-expert
description: High-fidelity SaaS wireframing guide focusing on conversion funnels, exact screen dimensions (1440x1024 / 393x852), and real-content strategies. Use when designing Landing Pages, Dashboards, and B2B user flows.
---

# SaaS Wireframe Expert

This skill enforces strict, industry-standard conversion and utility patterns for SaaS applications.

## Core Directives

1. **NO LOREM IPSUM:** Never use placeholder text. Inject highly specific, industry-accurate mock data to validate Information Architecture.
   - *Wrong:* `[Product Name] - [Price]`
   - *Right:* `Xiaomi Air Purifier TH - ฿1,500 (+14% YoY)`
2. **Skip Lo-Fi:** If a design system (like Fluent 2) is established, jump straight to High-Fidelity layout mapping. Do not waste time on abstract skeleton boxes.
3. **Target Exact Canvas Sizes:**
   - **Desktop (Dashboards):** 1440px wide by 1024px tall.
   - **Mobile (Landing Pages/Social flows):** 393px wide by 852px tall.

## 1. Landing Page Specifications (Conversion Focus)

The goal is to move the user from "What is this?" to "Sign up" in under 10 seconds. Mobile-first design is mandatory if distributed via social channels (WeChat, Zhihu).

*   **Hero Section (Above the Fold):**
    *   **H1:** Max 8 words. Benefit-led, not feature-led (e.g., "Find Winning Shopee Products Before Competitors").
    *   **Sub-H1:** 1-2 sentences explaining the exact mechanism (e.g., "AI-powered market research combining live Shopee data and TikTok trends").
    *   **Primary CTA:** High-contrast button with action-oriented text (e.g., "Get Free Market Report").
    *   **Visual:** High-fidelity dashboard teaser or sample report.
*   **Social Proof (The Trust Bar):**
    *   Grayscale logos immediately below the fold (e.g., Data sources like Shopee/TikTok, or beta client logos).
*   **Features Grid:**
    *   3-column layout. Icon + Benefit (Focus on outcomes, e.g., "ROI Estimation" > "Calculator").
*   **Footer CTA:**
    *   Repeat the primary CTA at the bottom of the page to catch scrolling users.

## 2. Dashboard Specifications (Utility Focus)

The dashboard is Mission Control. It must prioritize clarity and reduce cognitive overload.

*   **Global Layout (1440px):**
    *   **Left Sidebar (240px wide):** Global Navigation (Overview, Discovery, Reports, Settings).
    *   **Top Navbar (64px high):** Search, User Profile, Export CTA.
    *   **Main Content Area (1200px wide):** 24px padding on all sides.
*   **The F-Pattern Hierarchy:**
    *   **Top-Left:** The single most critical metric.
    *   **Top Row:** 3-4 Scorecard widgets (KPIs like Growth %, Sentiment, Market Cap).
*   **Data Visualization Rules:**
    *   **Line Charts:** Use for trends over time.
    *   **Tables:** Use for granular data. Must include Sorting, Filtering, and Pagination controls.
*   **Progressive Disclosure:**
    *   Do not show all data at once. Keep the main view clean.
    *   Use "View Details" buttons or slide-out Drawers (800px wide) for deep dives into specific entities.
*   **Actionability (B2B Crucial):**
    *   Always include prominent "Export to PDF/CSV" or "Share" buttons. B2B users must present data to their stakeholders.

## 3. Workflow & Output Checklist

When creating a SaaS wireframe, you must explicitly confirm:
- [ ] Is it sized correctly? (1440x1024 or 393x852)
- [ ] Does it use specific, realistic domain data?
- [ ] Is the primary CTA obvious and action-oriented?
- [ ] Is progressive disclosure utilized to hide secondary data?
- [ ] Does it pass the "No Instruction" test? (Can a user find the core feature without explanation?)
