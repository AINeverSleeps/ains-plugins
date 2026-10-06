---
name: consulting-os
description: "Use for any consulting or advisory work: framing a vague brief, hypotheses and issue trees, market sizing, research and interview synthesis, models, business cases and valuation, proposals and statements of work, storylines, ghost decks and slides, steering packs, workshops and client management. Loads the right method from the AINS Consulting OS library and follows it."
---

# AINS Consulting OS

You have the AINS Consulting OS connector (the `consulting-os` MCP server): Jonathan Chan's library of consulting methods. Each method is a full skill: when to use it, the steps, worked examples and the evidence controls. The library is served live, so it is always the current version.

## How to work

1. **Pick the method.** If the user names one, use it. Otherwise call `list_methods` once and choose the best fit from each method's "when to use" line. The catalog below helps you shortlist. `find_methods` is only a keyword shortcut.
2. **Load it.** Call `get_method` with the method name and follow it step by step: ask for the inputs it asks for, calculate in code where it says to, and apply its evidence controls.
3. **Load supporting files only when needed.** When the method refers to its toolkit (templates, checklists, drills) or decision controls, call `get_method_file` with the path it lists, such as `references/toolkit.md`.
4. **Chain methods for bigger jobs.** A typical engagement runs: `hypothesis-driven-problem-solving` → `structured-thinking-mece` → research and analysis methods → `getting-to-the-so-what` → `storylining` → `ghost-deck-and-deck-review`.

## Non-negotiables

- **De-identify first.** Before working on client material, run `de-identify` unless the user confirms it is already clean or fictional.
- **Check every number.** Before a deliverable leaves the user's hands, run `verify-my-numbers`.
- **Never invent** client facts, figures, quotes or sources. If an input is missing, ask for it or mark the assumption clearly.

## Catalog (choose with `list_methods`, load with `get_method`)

- **ai-workflow**: `claude-md-builder`, `client-project-setup`, `context-manager`, `de-identify`, `deliverable-designer`, `scheduled-automation`, `verify-my-numbers`, `write-your-own-skill`
- **analytics-modeling**: `large-dataset-analytics`, `market-research-basics`, `modeling-and-analysis`, `primary-research`
- **business-development**: `discovery-and-qualification`, `engagement-scoping-and-contracting`, `proposal-writing`
- **client-management**: `client-capability-building`, `coaching-feedback-and-reviews`, `engagement-close`, `execution-governance`, `personal-effectiveness`, `project-leadership-and-workplanning`, `stakeholder-and-change-management`, `status-and-steering-reports`, `working-with-clients`
- **communication**: `delivery-and-discussion`, `effective-slidewriting`, `executive-presence`, `ghost-deck-and-deck-review`, `meeting-facilitation`, `storylining`, `written-communication`
- **consulting-methodology**: `back-of-envelope-analysis`, `fast-knowledge-search`, `getting-to-deeper-insight`, `getting-to-the-so-what`, `hypothesis-driven-problem-solving`, `issue-analysis-flow-logic`, `option-comparison`, `structured-thinking-mece`
- **finance**: `commercial-due-diligence`, `financial-analysis-basics`, `investment-analysis-capital-budgeting`, `valuation-and-dcf`
- **functional-expertise**: `ai-opportunity-assessment`, `business-unit-strategy`, `cost-reduction-program`, `game-theory-and-scenario-planning`, `lean-operations`, `organisation-design`, `pricing-strategy`, `sales-force-effectiveness`

## If the tools are missing or refuse access

The library needs an active AINS API key. Tell the user:

- **Claude Code:** run `/plugin configure consulting-os@aineversleeps` and paste the key.
- **Claude app (web, desktop, Cowork):** Customize > Connectors > the AINS Consulting OS connector, with the key as the API key / bearer token.
- **Get or check a key:** https://www.aineversleeps.net/members/consulting-os

Do not try to reproduce a method from memory when the library is unavailable. Say what is missing.
