---
name: a11y
description: Accessibility guidance so everyone can use an interface: keyboard use, focus, color contrast, semantic HTML, ARIA, screen readers, forms, motion, touch targets and WCAG 2.2 AA. Use whenever the user asks for an accessibility audit or fix, mentions a11y, WCAG, screen readers, keyboard navigation, contrast or "acessibilidade", or is building interactive UI such as forms, menus, dialogs, tabs, dropdowns and custom components, even if they never say "accessibility". Use alongside `ui` and `ux`, because accessibility is easiest to get right while building.
---

# Accessibility

An interface is only finished when people can use it without a mouse, without seeing color, with a screen reader, with large text, or with limited motor control. These are everyday conditions, not edge cases: temporary injuries, bright sunlight and a broken trackpad create them for everyone. The practical goal is WCAG 2.2 level AA, built in from the start because retrofitting it costs far more.

## Process

1. **Start with the right element.** Most accessibility comes from using the correct semantic HTML (`button`, `a`, `label`, `nav`, `main`, `h1`-`h6`, `ul`, `table`). Custom elements need everything the native one gave for free. Read [references/semantics-and-aria.md](references/semantics-and-aria.md) when building or reviewing structure and custom widgets.
2. **Make it work with the keyboard.** Every action reachable and operable, with a visible focus and a logical order. Read [references/keyboard-and-focus.md](references/keyboard-and-focus.md) for interactive pieces, dialogs, menus and flows.
3. **Check perception.** Contrast, text size, color-only meaning, motion and zoom. Read [references/visual-and-motion.md](references/visual-and-motion.md) when choosing colors, type, charts, animation or media.
4. **Check forms and messages.** Read [references/forms-and-feedback.md](references/forms-and-feedback.md) for inputs, errors, status updates and loading.
5. **Run [references/audit-checklist.md](references/audit-checklist.md)** on your own output and fix failures. When asked for an audit, report findings by severity with the element, the problem, who it affects and the fix.

## Principles

- **Native first, ARIA second.** The first rule of ARIA is to not use it when a native element exists. Wrong ARIA is worse than none.
- **Don't rely on one sense.** Color, sound, position or hover alone must never carry meaning.
- **Don't take control away.** No keyboard traps, no autoplay that cannot be stopped, no time limits without a way to extend them.
- **Automated tools find about a third of the problems.** Pair them with a keyboard pass and, when possible, a screen reader pass. Do not claim an interface is "fully accessible" from a tool score alone.
- **Report what you did not verify.** If you could not run the page, a screen reader or a contrast tool, say so.

## Working with the other skills

`ui` chooses color, type and motion, and accessibility sets the floor: contrast, focus visibility and reduced motion override a visual preference. `ux` decides structure and flow, and accessibility makes that structure operable and announced correctly. `copy` and `ux/references/writing.md` supply clear labels, error text and link text, which screen reader users depend on.

## Source

Numeric thresholds in the references were checked against the WCAG 2.2 text published by the W3C (https://www.w3.org/TR/WCAG22/) on 2026-10-07: contrast 4.5:1 and 3:1, non-text contrast 3:1, target size 24 by 24 CSS pixels, reflow at 320 CSS pixels, text resize at 200%, text spacing values, three flashes in one second, and pause controls after 5 seconds. When a legal requirement applies, confirm against the current standard and the applicable local law.
