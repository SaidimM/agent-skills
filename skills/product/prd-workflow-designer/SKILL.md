---
name: prd-workflow-designer
description: Discover requirements from vague feature requests, ask targeted clarification questions, review technical and hardware feasibility, draft Product Requirement Documents (PRDs), and design user, system, and integration workflows. Use when turning an initial idea into a structured PRD package with assumptions, architecture/system diagrams, flow definitions, risks, and review-ready revisions.
---

# PRD & Workflow Designer

Treat the first user request as an intake signal, not a complete specification. If the request is vague, do not jump straight to the PRD. Discover the real requirement first, then draft a reviewable specification package.

## Core Approach

Filter the request through these lenses before drafting anything:

1. **Why:** Identify the underlying problem, business need, or operational pain point.
2. **Who:** Identify the primary actor, operator, or stakeholder.
3. **What:** Identify the desired capability, scope boundary, and expected outputs.
4. **How:** Identify the systems, interfaces, workflows, and constraints involved.
5. **So What:** Identify measurable success criteria, operational impact, and risks of failure.

Always separate:
- `Confirmed`
- `Inferred`
- `Unknown`

## Workflow

### Step 1: Frame the Request

Rewrite the user request into a short problem statement.

Capture:
- user goal
- triggering event or scenario
- target users or operators
- expected outcome
- obvious ambiguities

If the request already contains assumptions, surface them explicitly instead of silently accepting them.

### Step 2: Ask Targeted Discovery Questions

Ask a focused set of high-value questions to close the biggest gaps. Do not ask open-ended questions forever.

Prefer one short batch that covers the most important unknowns:
- business objective
- primary user or operator
- current workflow
- desired future workflow
- inputs and outputs
- integration points
- success criteria
- operational constraints
- hardware or environment dependencies
- must-have vs nice-to-have scope

Use follow-up questions only when the answers materially change the PRD or design.

If the request is about a technical workflow, test automation, infrastructure, devices, or integrations, ask questions that expose hidden system requirements such as:
- orchestration responsibilities
- system ownership boundaries
- APIs or protocols already available
- required logs, events, and observability
- real hardware vs simulated components
- error handling and recovery expectations

### Step 3: Review Technical and Hardware Reality

Before finalizing the spec, inspect what actually exists.

Review, when applicable:
- codebase structure and existing modules
- available APIs, handlers, services, and scripts
- device communication paths
- simulator capabilities
- hardware dependencies
- environment constraints
- missing interfaces or unclear ownership

Treat feasibility review as part of requirements discovery. If a desired workflow depends on components that do not exist yet, state that explicitly as a proposed design decision, not an established fact.

### Step 4: Synthesize the System Model

Translate the discovered requirements into a concrete system model before writing the final PRD.

Define:
- major components and responsibilities
- control flow and data flow
- user actions and system reactions
- subsystem boundaries
- interface touchpoints
- failure and recovery paths

When the request is technical or integration-heavy, include the most useful design artifacts, such as:
- component or system architecture diagram
- sequence or interaction flow
- operational workflow
- user flow or GUI flow

Prefer Mermaid or structured text diagrams unless the user requests a different format.

### Step 5: Draft the Specification Package

Produce a draft package, not just a PRD.

The draft package should contain:
- problem statement
- confirmed requirements
- assumptions to validate
- open questions
- PRD draft
- workflow or GUI flow
- system architecture or integration flow
- risks, dependencies, and out-of-scope items

For PRD structure, read [references/prd-template.md](references/prd-template.md).

For GUI and interaction flow quality checks, read [references/gui-workflow-checklist.md](references/gui-workflow-checklist.md).

### Step 6: Run the Review and Revision Loop

Treat the first output as a review draft unless the user explicitly asks for a final version.

Invite review on:
- incorrect assumptions
- missing requirements
- priority changes
- technical constraints
- workflow corrections
- diagram corrections

When the user gives feedback, revise the package by separating:
- what changed
- why it changed
- what remains unresolved

### Step 7: Finalize the Approved Version

When the user confirms alignment, produce a clean final package with:
- approved scope
- final requirements
- final acceptance criteria
- final diagrams or flows
- explicit out-of-scope
- implementation dependencies
- remaining risks or follow-up decisions

## Output Rules

- Be concise. Prefer bullets, short tables, and compact sections.
- Make acceptance criteria binary and testable.
- Include explicit out-of-scope items.
- Distinguish confirmed facts from assumptions and unknowns.
- Make every user action and system action produce a corresponding reaction or outcome.
- Do not present inferred architecture as existing reality without evidence.
- Do not let discovery stall indefinitely. After the key questions are answered, draft the first version and mark unresolved items clearly.
- If the user request is highly technical, include both product language and system design language.
