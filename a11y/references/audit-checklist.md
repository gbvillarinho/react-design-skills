# Audit checklist

Run this on your own output, or use it as the structure of an audit. For each failure, record: **where** (element or screen), **what is wrong**, **who it affects**, **severity** and **the fix**.

Severity: **Blocker** (a task cannot be completed), **Serious** (completing it is very hard), **Moderate** (confusing or tiring), **Minor** (polish).

## Structure
- [ ] `lang` is set, each page has a unique title, one `h1`, and headings in logical order.
- [ ] Landmarks exist (`header`, `nav`, `main`, `footer`), and a skip link is the first focusable item where navigation repeats.
- [ ] Buttons are `button`, links are `a href`, and lists and tables use real list and table markup.
- [ ] Images have suitable `alt` (empty for decorative), and icon-only controls have names.
- [ ] Link and button text makes sense out of context.

## Keyboard
- [ ] Everything operable with the keyboard, in a logical tab order, with no traps.
- [ ] Focus is always visible, with at least 3:1 contrast, and never hidden behind sticky UI.
- [ ] Dialogs move focus in, contain it, return it on close, and close with Escape.
- [ ] Hover content also appears on focus; drag actions have a non-drag alternative.
- [ ] Touch targets are at least 24 by 24 CSS pixels (aim for 44).

## Visual
- [ ] Text contrast is at least 4.5:1 (3:1 for large text); UI components and chart marks at least 3:1.
- [ ] Meaning is never carried by color alone.
- [ ] The page reflows at 320px width and 200% zoom, and pinch zoom is allowed.
- [ ] `prefers-reduced-motion` is respected; nothing flashes; auto-moving content can be paused.

## Forms and feedback
- [ ] Every input has a visible, associated label; grouped controls use `fieldset` and `legend`.
- [ ] Required fields are marked in visible text (and with `required`), and the legend or note explaining the mark is on the page.
- [ ] Forms and landmark regions that appear more than once (or inside `aside` or `section`) have an accessible name.
- [ ] Errors say what went wrong and how to fix it, are linked to their field, and focus moves to the first one.
- [ ] Status updates are announced (live regions) without stealing focus.
- [ ] Input types and `autocomplete` are set; paste is allowed.

## Custom components
- [ ] Each custom widget follows the keyboard pattern for its role, and exposes name, role and state.
- [ ] ARIA is used only where native HTML cannot do the job, and `aria-hidden` is not on anything focusable.

## Verification
- [ ] I tabbed through the whole page.
- [ ] I ran an automated check (for example axe or Lighthouse), or I state that I did not.
- [ ] I tested with a screen reader, or I state that I did not and which areas remain unverified.

## Reporting
Summarize results by severity, list what is verified and what is not, and avoid saying "fully accessible". Automated tools cover only part of the standard.
