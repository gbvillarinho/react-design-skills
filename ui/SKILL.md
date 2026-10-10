---
name: ui
description: Visual design guidance for distinctive, non-template interfaces: look and feel, visual identity, typography, color palette, hero, layout style and motion. Use whenever the user wants a screen, landing page, site, app or dashboard to look better, have its own identity or stop looking generic, even if they never say "UI". For usability, placement of elements, flows, forms and microcopy, use the `ux` skill alongside this one.
---

# Design

Approach this as the design lead at a design studio known for giving every client a distinct visual identity that is not mistaken for anyone else's. This client has already rejected proposals that felt cliché or templated, and is paying for a distinctive point of view: make deliberate, opinionated choices about palette, typography, and layout that are specific to this brief, and take aesthetic risk if justified.

## Respect what already exists

Before any decision, check whether the project already has a design system, tokens, fonts, a palette or components. If it does, they take priority: keep them and apply the guidance below only on the axes left open. This skill is for creating identity where none exists yet, not for replacing one that has already been chosen.

## Ground your designs in the subject matter

If the brief does not identify what the product or subject matter is, identify it before designing and confirm with whoever asked. Propose one concrete subject, the design's audience, and the design's primary job. If you have any information about their preferences or what they're building, use it as a hint. The subject's industry, materials, and vernacular are where distinctive visual choices come from — a design for a toy for girls aged 8–11 will be very aesthetically different from a dashboard for financial analysts. Build with the brief's real content and subject matter throughout.

## Design principles

For web designs, the hero is the first thing viewers will see. Open with the most characteristic thing in the subject's world, in the form that is most appropriate: a headline, an image, an animation, a live demo, an interactive moment, or other treatments. Be deliberate with your choice: a big number with a small label, supporting stats, and a gradient accent is the default treatment, so only use it if that's truly the best option.

Typography carries the personality of the page. You don't need a different typeface for display or headline text and body content: use one family or two, and if two, make them clearly distinct.

Choose your typefaces deliberately, not the default families you would reach for on any other project, and set a clear type scale following the default guidance of The Elements of Typographic Style with intentional weights, widths, and spacing. When type is used as a headline or visual element, use the type treatment itself as an active part of the design, not a neutral delivery vehicle for the content.

Default to line lengths of less than 80 characters. Serif typefaces can have slightly longer line lengths; give serif body text slightly more line-height than a sans-serif.

Avoid these default typographic treatments; they are the commonest tells of a generated page:
- Accenting just a single word or phrase in a headline, like putting one word in italic/bold or a different color.
- Using all caps for labels.
- Adding unnecessary typographic labels above content.

Visual structure is information. Structural devices like outlines, borders, numbering, eyebrows, dividers, labels, etc., encode useful information about the content rather than decorate it. Many generic designs use numbered markers (01 / 02 / 03), but that's only appropriate if the content actually is a sequence — like a stepped process or a timeline. Before adding numbered markers, check the content really is a sequence.

Use non-user-triggered motion sparingly and deliberately, only to draw attention. A single orchestrated moment — one page-load sequence or one reveal — lands better than scattered effects; fade-and-slide-up entrances on each section and hover transitions on every card are the generic default and read as AI-generated. Motion that answers a person's action (opening, expanding, confirming) is welcome when it shows what changed.

Consider written content carefully. Often a design brief may not contain real content, and it's up to you to come up with copy and placeholder content. Copy can make a design feel as templated as the design itself. Follow the `ux` skill's writing reference for this.

## Process: plan, review against the brief, build, critique

Before planning, read [references/cliches.md](references/cliches.md): it lists the most common generic patterns in AI-generated design. They are legitimate for some briefs, but they are defaults, not choices. Where the brief pins down a visual direction, follow it exactly, even if it asks for one of these looks. Where it leaves an axis free, don't spend that freedom on them, and don't swap one cliché for the same substitute every time: genuinely vary between projects.

For images, photos, illustration and placeholders, read [references/imagery.md](references/imagery.md). For anything that animates, read [references/motion.md](references/motion.md).

Before choosing a layout, read [references/composition.md](references/composition.md): compose on purpose, sketch more than one structure, and add one twist so the page does not read as the default.

To see how to go from a subject to a visual direction, see [references/subject-examples.md](references/subject-examples.md).

Work in two passes. First, brainstorm a short design plan based on the brief: create a compact token system with color, type, layout, and principles.
- Color: describe the core base palette as 4–6 named hex values.
- Type: the typefaces and their roles.
- Layout: a layout concept, using one-sentence prose descriptions and ASCII wireframes to ideate and compare. Compare at least two structurally different compositions and pick one that is not the default split hero with stacked sections. Include alignment guidance; should the content be left aligned, center aligned, justified?
- Principles: the high-level guidance for what makes this page unique.

Then review that plan against the brief before building: if any part of it reads like the generic default you would produce for any similar page (work through a similar prompt to see if you arrive somewhere similar) rather than a choice made for this specific brief — revise that part, say what you changed and why. Only after you've confirmed the relative uniqueness of your design plan should you start to write the code, following the revised plan.

When writing the code, be careful of structuring your CSS selector specificities. It's easy to generate CSS classes that cancel each other out (especially with a type-based selector like .section and an element-based selector like .cta). This can happen often with padding/margin between sections.

## Data and charts

Color in a chart carries meaning, and every mark needs a reason to exist. Neutral for ordinary data, one accent for what needs attention. For any chart, KPI or number-heavy view, use the `dataviz` skill and `ux/references/data-display.md`.

## Scale and finish

Components should look sized to their role. Inputs and buttons that are much taller, wider or heavier than the content around them make a screen feel clumsy. Keep a consistent scale, and check each element against its importance.

Do not draw complex objects (food, people, products) in CSS or SVG; use a marked placeholder instead. See `references/composition.md`.

## Restraint and self-critique

Spend your boldness in one place. Let one element be the memorable thing, keep everything around it quiet and disciplined, and cut any decoration that does not serve the brief. Build to a quality floor without announcing it: responsive down to mobile, visible keyboard focus, reduced motion respected, visually accessible, harmonious color palettes. Critique your own work as you build, taking screenshots to review if your environment supports it — a picture is worth 1000 tokens. Consider Chanel's advice: before leaving the house, take a look in the mirror and remove one accessory. Human creatives have memory and always try to do something new, so if you have a space to quickly jot down notes about what you've tried, it can help you in future passes.

## Working with the `ux` skill

This skill decides how the interface looks. The `ux` skill decides what goes where and how it behaves: hierarchy, flows, states, forms and microcopy. When both apply, settle placement and behavior with `ux` first, then give it a visual identity here. Buttons, error messages, empty states and placeholder copy follow `ux/references/writing.md`.

Text on the page (headlines, hero lines, section copy) is the job of the `copy` skill. Generic wording undoes a distinctive visual design, so write or review it there.


Accessibility sets the floor for visual choices: contrast, focus visibility, text size and reduced motion override a visual preference. For audits and interactive components, use the `a11y` skill.
