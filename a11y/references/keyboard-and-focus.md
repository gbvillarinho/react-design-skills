# Keyboard and focus

## Basics

- Every interactive element works with the keyboard: Tab and Shift+Tab to move, Enter to activate links and buttons, Space for buttons and checkboxes, arrow keys inside composite widgets, Escape to dismiss.
- **Tab order follows the visual and logical order.** Fix the DOM order rather than using positive `tabindex`. Use `tabindex="0"` only to make a custom widget focusable and `tabindex="-1"` for elements that receive focus by script.
- **Never remove the focus outline** without a replacement that is at least as visible. A solid 2px or thicker outline with at least 3:1 contrast against its surroundings, offset from the element, is a safe default. Use `:focus-visible` to show it for keyboard users.
- **Focus must not be hidden** behind sticky headers, cookie banners or chat widgets. AA (2.4.11) requires that a focused item is not *entirely* covered; making it fully visible is the stricter AAA level (2.4.12) and the better practice. Use `scroll-padding` so focused elements scroll into view.
- **No keyboard traps.** A person who tabs into a component must be able to tab out, except inside a modal dialog that closes with Escape.
- **Single-key shortcuts** need a way to turn off or remap, so they do not collide with speech input.

## Focus management

| Moment | What to do |
|---|---|
| Opening a dialog | Move focus to the dialog (its first control or the title), contain it, and make the page behind inert |
| Closing a dialog | Return focus to the control that opened it |
| Route change in a single-page app | Move focus to the new page's heading or main region, and update the document title |
| Inline content appears (an error, a new section) | Move focus only if the person needs to act on it; otherwise announce it with a live region |
| Content is removed | Move focus to a sensible neighbor, not to the top of the page |
| Failed submit | Move focus to the first error or to an error summary with links |

## Pointer and touch

- **Target size:** WCAG 2.2 AA (2.5.8) requires at least 24 by 24 CSS pixels. Smaller targets pass only through an exception, mainly spacing (a 24px circle centered on each target must not touch another target), an equivalent control on the same page, inline links in a sentence, browser-controlled controls, or when the size is essential. 44 by 44 is the stricter AAA level (2.5.5) and a good aim for primary touch targets.
- **Don't depend on hover.** Anything revealed on hover must also appear on focus, and not vanish when the pointer moves onto it.
- **Provide alternatives to dragging and multi-finger gestures:** buttons or inputs that do the same job (WCAG 2.2 dragging movements).
- **Pointer cancellation:** trigger actions on release (`click`), not on press, so people can move away to cancel.
- **Don't trap scroll** inside nested containers without a way out.

## Time and interruptions

- Let people extend, pause or turn off time limits, auto-advancing carousels and auto-updating content.
- Don't autoplay audio. If video autoplays, keep it muted and give a visible pause control.
- Avoid unexpected context changes when a control receives focus or its value changes (no automatic navigation on select).
