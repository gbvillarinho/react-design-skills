# Semantics and ARIA

## Use the right element

| Need | Use | Not |
|---|---|---|
| Something that does an action | `<button type="button">` | `<div onclick>` or `<a>` without a destination |
| Navigation to another page or section | `<a href>` | A button that changes `location` |
| Page regions | `<header>`, `<nav>`, `<main>`, `<aside>`, `<footer>`, `<section>` with a heading | A pile of `<div>`s |
| Headings | `<h1>` once, then `<h2>`/`<h3>` in order, without skipping levels | Bold text styled as a heading, or levels chosen for size |
| Lists of items | `<ul>`/`<ol>`/`<li>` | Line breaks between items |
| Tabular data | `<table>` with `<th scope>` and a `<caption>` | A grid of divs |
| Inputs | `<label for>` tied to an `<input>`, `<select>`, `<textarea>` | A placeholder acting as the label |
| Images | `<img alt>` | Missing `alt`, or filenames as alt text |

Also: set `lang` on `<html>` (and on passages in another language), give each page a unique `<title>`, and provide a "skip to main content" link as the first focusable element on pages with repeated navigation.

## Alternative text

- **Informative image:** describe what it communicates in context, briefly.
- **Decorative image:** `alt=""` so screen readers skip it.
- **Image inside a link or button:** describe the destination or action, not the picture.
- **Charts and complex images:** a short alt that states the main finding, plus the data in a nearby table or text.
- **Icons without text:** an accessible name (`aria-label` or visually hidden text). Icons beside text are decorative.

## Link and button text

- Say where it goes or what it does ("Download the price list (PDF)"), not "click here" or "read more".
- Two links with the same text must go to the same place.
- A button that opens something is named for the action, and its state is exposed (`aria-expanded`).

## When ARIA is needed

Use ARIA only to add what HTML cannot express, such as custom widgets, live regions and relationships.

- **Names and descriptions:** `aria-label`, `aria-labelledby`, `aria-describedby`.
- **State:** `aria-expanded`, `aria-pressed`, `aria-selected`, `aria-current`, `aria-checked`, `aria-invalid`, `aria-disabled`.
- **Live regions:** `role="status"` or `aria-live="polite"` for non-urgent updates, `role="alert"` for urgent errors. The container must exist in the DOM before its content changes.
- **Hiding:** `aria-hidden="true"` removes content from assistive tech, so never put it on focusable elements or on content people need.
- **Roles on custom widgets** (tabs, menus, dialogs) require the keyboard behavior that goes with them. If you cannot implement that behavior, use native elements or a simpler pattern.

## Common custom patterns

- **Dialog:** `role="dialog"` (or `<dialog>`), `aria-modal`, labeled by its title, focus moves in on open, stays inside, and returns to the trigger on close; Escape closes it.
- **Disclosure / accordion:** a `button` with `aria-expanded` controlling a region. Prefer this over complex tab or menu roles.
- **Tabs:** `tablist`, `tab`, `tabpanel`, arrow keys to move between tabs, only the active tab in the tab order.
- **Menus:** a "menu" role is for application-style menus. For site navigation, use a list of links, optionally with a disclosure button.
- **Tooltips:** content must also be reachable by keyboard focus and not be the only place essential information lives.
