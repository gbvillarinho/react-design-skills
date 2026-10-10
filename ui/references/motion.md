# Motion

Motion should explain what changed or direct attention. If it does neither, it is decoration, and decoration reads as generated. The core rule of this skill still holds: one orchestrated moment beats scattered effects.

## Default to instant

Start from no animation and add motion only when it earns its place. People often want the result immediately, and every animation makes them wait, even a short one, and the cost repeats each time they do the same thing.

- **Frequency decides.** The more often an action happens, the less motion it should have. Actions people repeat all day (opening menus, switching tabs, toggling filters, typing, saving, navigating lists) should feel instant: no transition, or a change so short it is barely noticed. Save richer motion for rare moments (first load, a completed purchase, onboarding).
- **Never block.** The interface must accept the next action while something animates. Do not make people sit through an intro, a transition between routes or a staged reveal before they can read or click.
- **Content before choreography.** Show the content immediately and let any motion run alongside it, not in front of it.
- **Speed is part of UX.** Under about 100 ms feels instantaneous, around 1 second keeps the person's flow, and beyond that they notice waiting. A 400 ms transition on a common action is slow. Responses to input should show something within about 100 ms.
- **Cut when in doubt.** If removing an animation changes nothing about understanding, remove it. Ask of each one: what does the person lose without it?
- **Let people opt out.** Respect reduced motion, and consider a faster or no-animation option in tools used all day.

## Two kinds of motion

| Kind | Role | Guidance |
|---|---|---|
| **Responsive** (answers a person's action) | Shows what changed: opening, expanding, confirming, reordering | Welcome, but keep it short and tied to the action |
| **Ambient** (starts by itself) | Draws attention or sets mood | Rare. One per page, with a clear reason, and easy to stop |

Avoid the generic defaults: fade-and-slide-up on every section, hover lift on every card, parallax everywhere, looping decorative animation.

## Choosing the one moment

Ask what single thing the page most wants people to notice or understand, then give motion to that. Good candidates:

- A live element tied to the subject (a countdown, a filling progress bar, a ticking schedule).
- A reveal that explains something (a chart drawing in, a before and after).
- A load sequence that introduces the main headline and call to action.
- A single interaction the page is built around (playable keys, a configurator).

Everything else stays still, so the moment reads.

## Timing and easing

- **Duration:** these are ceilings, not targets. About 100 to 150 ms for small feedback (hover, press, toggles), 150 to 250 ms for panels and dialogs, up to about 400 ms for a larger reveal on a rare moment. For frequent actions use less, or none. Longer than that feels slow unless it is the featured moment.
- **Easing:** ease-out for things entering (fast start, gentle stop), ease-in for things leaving, ease-in-out for movement across the screen. Avoid linear except for continuous loops like spinners.
- **Move less:** short distances (8 to 24 px) feel more refined than long slides. Prefer opacity and transform.
- **Stagger with restraint:** 30 to 80 ms between items, and only for a short list. Long staggers feel like waiting.
- **Consistency:** reuse the same few durations and curves across the page, as you would a type scale. Define them as tokens (CSS variables).

## Performance and craft

- Animate `transform` and `opacity`. Avoid animating layout properties (`width`, `height`, `top`, `left`) because they cause reflow.
- Use `will-change` sparingly and only while something animates.
- Keep layout stable: reserve space for anything that appears, so nothing jumps.
- Prefer CSS transitions and keyframes. Use JavaScript for sequencing or when the motion depends on data or input.
- Do not block interaction while something animates.

## Accessibility (non-negotiable)

- Respect `prefers-reduced-motion`: replace movement with a fade, or remove it. Content must still be complete without animation.
- Nothing flashes more than three times per second.
- Anything that moves automatically for more than five seconds needs a way to pause or stop it.
- Never hide information that only appears on hover or after an animation without a keyboard and touch alternative.
- See the `a11y` skill for the full rules.

## Checklist

- [ ] Frequent actions are instant, and nothing makes the person wait or blocks the next action.
- [ ] There is at most one ambient moment, and I can say why it is there.
- [ ] Responsive motion is short and shows what changed.
- [ ] Durations and easings come from a small shared set.
- [ ] Only `transform` and `opacity` are animated for movement.
- [ ] Reduced motion is respected and the page works with no animation.
