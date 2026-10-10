# Imagery and illustration

Images carry a large share of a page's personality, and they are where generated pages fail most visibly: crude drawings, generic stock scenes, decorative blobs. Decide what an image must do, then pick the honest way to provide it.

## Decide the job first

| Job | Good answer |
|---|---|
| Show the real thing (food, place, product, people) | A real photo. If you do not have one, a marked placeholder |
| Explain how something works | A diagram built from simple shapes and real labels |
| Show data | A chart (see `ux/references/data-display.md` and the `dataviz` skill) |
| Set a mood | Color, type, texture or pattern, not a fake photo |
| Mark a section or a feature | A small, consistent icon set, or none at all |

If an image does none of these jobs, leave it out. Empty space is better than decoration.

## What you can build well

- Typography, color fields, rules and grids.
- Geometric shapes and patterns that follow a rule (stripes, dots, grids, tiling).
- Diagrams, timelines, schedules, price lists and spec sheets using real content.
- Simple icons built from basic shapes, kept consistent in stroke and size.
- Real UI: a live widget, a demo or an interaction tied to the subject.

## What you should not draw

Food, animals, people, faces, hands, products, vehicles, landscapes and detailed scenes. In CSS or SVG they come out crude and make the whole page look cheaper. Do not draw them, even "simplified".

## Placeholders that help

When a photo or illustration would improve the page and you cannot supply it:

- Reserve the space with a fixed `aspect-ratio`, so the layout does not shift when the real image arrives.
- Mark it clearly as a placeholder in the page, not as if it were finished.
- Write a short **shot brief** inside or beside it: subject, framing, light, setting, and what must be visible ("cut loaf, crumb in focus, window light, wooden counter"). The owner can hand that to a photographer or a generator.
- Tell the person in your summary which images they need to supply, with sizes.

## Photo direction (for when real images exist)

- Prefer tight crops and real details over wide generic scenes.
- Keep one consistent treatment (color grade, aspect ratios, framing) across the page.
- Show real people and places of the business when possible; avoid stock smiles.
- Place the focus where the layout needs it with `object-position`, and test crops at mobile and desktop widths.

## Technical basics

- Provide `width`, `height` or `aspect-ratio`, `loading="lazy"` for below-the-fold images, and modern formats where available.
- Use `srcset` and `sizes` for responsive images.
- Every informative image needs useful alt text, and decorative images need `alt=""` (see the `a11y` skill).
- Do not put essential text inside an image.
