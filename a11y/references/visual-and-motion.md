# Perception: contrast, type, color, motion

## Contrast (WCAG AA)

| Element | Minimum contrast |
|---|---|
| Body text and text in images | 4.5:1 |
| Large text (18pt or larger, or 14pt bold or larger; about 24px, or 18.66px bold) | 3:1 |
| UI components: input borders, icons that carry meaning, focus indicators, chart marks | 3:1 against adjacent colors |
| Disabled controls and decorative elements | No requirement, but keep them recognizable |

- Check the real colors, including text over images, gradients and hover or focus states. Light-gray placeholder text and pale borders are the most frequent failures.
- Check both light and dark themes.
- Verify with a tool instead of judging by eye. If you cannot run one, compute the ratio from the hex values and say it is unverified in a browser.

## Color is never the only signal

- State (error, success, selected, sold out), links inside text and chart series need a second cue: text, icon, pattern, underline, position or label.
- Red and green alone fail for color-vision deficiency. Pair them with a sign, an icon or a word.
- Charts: label values and series directly, and use shape or line style in addition to color.

## Text and zoom

- Use relative units (`rem`, `em`, `%`) so text scales with the user's settings. Body text at 16px or larger.
- The page works with text resized to 200% (1.4.4), and reflows at a 320 CSS pixel width without horizontal scrolling or lost content (1.4.10; 256 CSS pixels of height for content that scrolls horizontally).
- Do not block pinch zoom (`user-scalable=no`, restrictive `maximum-scale`).
- Support user text spacing overrides without loss of content (1.4.12): line height 1.5, paragraph spacing 2 times the font size, letter spacing 0.12 and word spacing 0.16 times the font size. That means no fixed heights that clip text, and no truncating essential text.
- Line length under about 80 characters, left aligned for long text, and enough line height (at least 1.5 for body text).
- Avoid justified text and long passages in all caps or italics.
- Don't use images of text unless it is a logo.

## Motion

- **Respect `prefers-reduced-motion`.** Remove or replace parallax, large movement, auto-scrolling and looping animation with a fade or no animation.
- **Nothing flashes more than three times per second.** This can trigger seizures.
- **Anything that moves, blinks or scrolls automatically for more than five seconds** needs a pause, stop or hide control.
- Motion that responds to a person's action is acceptable; keep it short and meaningful.

## Media

- Captions for prerecorded and live video with speech; a transcript for audio.
- Audio description or a text alternative when important information is visual only.
- Controls for media are keyboard accessible and labeled.

## Other preferences to honor

- `prefers-color-scheme` and `prefers-contrast` where practical, and `forced-colors` (Windows high contrast): don't rely on background images or color alone for meaning, and test borders and focus outlines there.
- Orientation: do not lock the page to portrait or landscape.
