---
name: ux
description: UX guidance for making interfaces usable: Nielsen's heuristics, visual hierarchy, where to place elements on the screen, reading patterns, user flows, the states every screen needs (empty, loading, error, success), forms, and microcopy. Use whenever the user is designing or reviewing a screen, flow, form, onboarding, navigation or dashboard, asks where something should go, says a screen is confusing, or wants a UX review, even if they never say "UX". For visual identity, palette and typography, use the `ui` skill alongside this one.
---

# UX

Good UX means a person finishes what they came to do without stopping to think about the interface. Visual polish does not fix a screen that makes people hunt for the next step, so settle structure and behavior before styling.

## Process

1. **Name the primary job.** Write one sentence: who is on this screen, and what do they need to finish? Everything else on the screen is secondary to that job. If the brief doesn't say, propose one and confirm.
2. **Check the locale.** Reading direction, date and number formats and cultural conventions change layout. "Left to right" does not hold for Arabic or Hebrew, so confirm the product's languages before applying placement rules.
3. **Pick the references that apply** and read only those:
   - Evaluating or designing any screen: [references/heuristics.md](references/heuristics.md)
   - Deciding what goes where, what is prominent, how the eye moves: [references/layout-and-hierarchy.md](references/layout-and-hierarchy.md)
   - Multi-step tasks, onboarding, destructive actions, anything that loads or can fail: [references/flows-and-states.md](references/flows-and-states.md)
   - Inputs, signup, checkout, settings: [references/forms.md](references/forms.md). Question which fields, steps and order are needed before designing.
   - Charts, KPIs, tables, dashboards: [references/data-display.md](references/data-display.md), and use the `dataviz` skill for any chart.
   - Buttons, labels, errors, empty states, interface microcopy: [references/writing.md](references/writing.md). For headlines, page text and reviewing text that sounds generic, use the `copy` skill.
4. **Build or revise**, keeping one primary action per view and a visible path forward.
5. **Run [references/review-checklist.md](references/review-checklist.md)** on your own output before finishing, and fix what fails.
6. **Report briefly** which rules shaped the layout, so the person can disagree with a specific decision instead of the whole design.

## Principles

- **Rules are tendencies, not laws.** Reading patterns, spacing rules and "best practices" are defaults for when you have no better information. If research on the real product, or the brief, contradicts them, follow the evidence.
- **Fewer decisions per screen.** Each extra option, link or field costs attention. Remove, group or defer before adding.
- **Show state, always.** People should know where they are, what happened and what they can do next.
- **Forgive mistakes.** Prefer undo over confirmation dialogs, and make errors explain the fix.
- **Respect people's time.** Speed is part of usability. Common actions should feel instant, and nothing, including animation, should make someone wait or block their next move.
- **Be consistent.** The same action looks and is named the same everywhere, so people learn the product once.

## Working with the `ui` skill

This skill decides what goes where and how it behaves. The `ui` skill decides how it looks. When both apply, settle structure here first, then style it with `ui`. If a visual choice from `ui` hurts usability (low contrast, a decorative label that hides meaning), usability wins.


For keyboard use, screen readers, contrast, focus management and audits, use the `a11y` skill; it makes the structure decided here operable and correctly announced.
