# Layout and hierarchy

Where the eye goes decides what people notice and do. Use these tendencies to place things, not to decorate.

## How people scan

- **F-pattern.** On text-heavy pages (articles, search results, documentation), people read the first lines across, then scan down the left edge. Put key words at the start of lines and headings.
- **Z-pattern.** On sparse pages (landing pages, simple screens), the eye moves across the top, diagonally down, then across the bottom. Put the logo or headline at the top, and the main action at the end of the path.
- **These are tendencies, not laws.** Strong contrast, faces, motion and size pull the eye away from either pattern. Check on the real design instead of assuming.
- **Reading direction changes everything.** "Left to right, top to bottom" applies to LTR languages. For RTL languages (Arabic, Hebrew), mirror the layout, including navigation, progress indicators and directional icons. Check the product's locales first.

## Hierarchy

- **One primary action per view.** If everything is emphasized, nothing is. Make the main action the most prominent, secondary actions quieter, and tertiary ones look like links.
- **Size, contrast, weight and space create order.** Decide what should be seen first, second and third, then check by squinting at the screen or blurring it.
- **Whitespace groups.** Space between groups should clearly exceed space inside a group, so the structure reads without lines.
- **Alignment makes scanning easy.** A shared left edge for labels, values and headings lets the eye run down the page. Avoid mixing center and left alignment in one block.
- **Titles say where you are.** Every screen has a visible name and, in deep flows, a sign of progress.

## Placement of common elements

- **Primary action:** at the end of the path the person follows (below the form, at the bottom of the card), aligned with the content it completes.
- **Navigation:** in a consistent place on every screen, with the current location marked.
- **Destructive actions:** apart from the primary action, and not styled like it.
- **Help and error messages:** next to what they refer to, not collected at the top.
- **Cancel and back:** present and predictable, never competing visually with the primary action.

## Mobile

- **Thumb reach.** The bottom of the screen is easiest to reach one-handed. Put frequent actions there, and rare or risky ones at the top or behind a menu.
- **Touch targets** should be at least about 44 by 44 points, with space between them.
- **One column, one job.** Prefer a single column with a clear sequence over shrinking a desktop layout.
- **Don't hide the essentials** behind a hamburger menu if people need them often.

## Dashboards and dense screens

- Put the answer to the person's main question first (the number or status they came for), then supporting detail.
- Group related metrics, and keep consistent positions for the same kind of data over time.
- Use color to carry meaning (state, change), not decoration.

## Action and navigation patterns

Knowing that "back should not compete with the primary action" is not enough; use the conventional shape. Compare:

| Situation | Do | Don't |
|---|---|---|
| Back in a multi-step flow | A back arrow at the top, next to the title, or a quiet text button below the primary action | A bordered button the same size as the primary one |
| Primary action | One filled button, full width on mobile, alone on its row | Two equal buttons side by side that make people choose |
| Cancel or skip | A text link or ghost button, smaller and lighter | A second filled button |
| Destructive action | Separate from the primary, red only at the point of commitment | Next to the primary with the same weight |
| Closing a dialog or sheet | An "x" in the corner, plus Cancel if data would be lost | Only a large "Close" button |

Only place two buttons side by side when both are real, equal choices (for example "Keep editing" and "Discard").

Proportion matters too. Controls should look sized to their importance: inputs and buttons tall enough to tap (about 44 to 48px) but not oversized, and a rhythm of spacing where related things sit closer than unrelated things. If a screen looks "out of scale", check that no component is much larger or heavier than its role deserves.
