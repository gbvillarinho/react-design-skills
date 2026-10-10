# Generic patterns to avoid

AI-generated design currently clusters around a few traits:

1. A warm cream background (near #F4F1EA) with a high-contrast serif display and a terracotta or warm-clay accent (often near #D97757 — Anthropic's own Claude-interaction accent, so on a user's brief it reads as a tell).
2. A near-black background with a single bright acid-green or vermilion accent.
3. A broadsheet-style layout with hairline rules, zero border-radius, and dense newspaper-like columns.
4. The SaaS-card kit: content chopped into identical rounded cards, one border-radius on everything regardless of hierarchy, the same soft grey shadow (rgba(0,0,0,.1)) under each, and gradient washes as decoration.
5. Template chrome that appears whatever the subject:
   - a tracked-out ALL-CAPS eyebrow label above every heading;
   - meta strings joined with middle dots ('A · B · C');
   - labels built as 'WORD — fragment' with a spaced em dash;
   - tinted near-black (#0B0B0B, #111) standing in for black;
   - a monospace face for small data labels;
   - a '→' appended to link and button text.
6. Structural sameness in page composition, which is the most common tell of all:
   - a split hero with text on the left and a picture or illustration on the right;
   - sections stacked one after another, each with a centered heading;
   - zigzag rows that alternate image and text;
   - a row of three feature cards, then a testimonial strip, then a centered call to action;
   - a plain footer with four link columns.
7. Hand-drawn objects in CSS or SVG (food, people, products, scenes). They almost always look crude, like a circle with two lines for a loaf of bread.

## How to use this list

All of these traits are legitimate for some briefs, but they are defaults rather than choices, and they appear regardless of subject.

- Where the brief pins down a visual direction, follow it exactly. The brief's own words always win, including when it asks for one of these looks.
- Where the brief leaves an axis free, don't spend that freedom on one of these defaults.
- Avoiding a cliché is not enough. If you always swap "cream + terracotta" for the same second option, that option becomes the new cliché. Genuinely vary between projects.
