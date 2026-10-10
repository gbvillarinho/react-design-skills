# Heuristics and laws

Use this list to evaluate a screen or to sanity-check a new design. For each item, ask the question and fix what fails.

## Nielsen's 10 usability heuristics

| Heuristic | Ask on this screen |
|---|---|
| 1. Visibility of system status | Does the person always know what is happening (loading, saved, sent, current step)? |
| 2. Match between system and real world | Do labels use the person's words, not internal terms? |
| 3. User control and freedom | Is there a clear way out: cancel, back, undo? |
| 4. Consistency and standards | Does the same thing look and behave the same everywhere, and follow platform conventions? |
| 5. Error prevention | Can the design stop the mistake before it happens (constraints, defaults, confirmations only for the risky)? |
| 6. Recognition rather than recall | Is what the person needs visible on screen, instead of something to remember from earlier? |
| 7. Flexibility and efficiency of use | Do frequent users have shortcuts, bulk actions or saved choices, without burdening newcomers? |
| 8. Aesthetic and minimalist design | Does every element earn its place? Is irrelevant information competing with relevant information? |
| 9. Help users recognize, diagnose and recover from errors | Does the error say what went wrong and how to fix it, in plain language? |
| 10. Help and documentation | Is help available where the confusion happens, short and task-focused? |

## Laws that guide layout and interaction

- **Fitts's law.** The time to hit a target depends on its size and distance. Make primary actions large and close to where attention already is. Keep destructive actions small, distant or confirmed.
- **Hick's law.** More choices means slower decisions. Reduce, group or reveal options in steps.
- **Miller's law.** People hold a handful of items in working memory. Chunk long lists, codes and forms into groups.
- **Jakob's law.** People expect your product to work like the others they use. Deviate only when the gain is clear.
- **Law of proximity and similarity (Gestalt).** Things placed close together, or styled alike, read as related. Use space and style to show grouping, not just borders.
- **Progressive disclosure.** Show the essentials first and reveal advanced options on demand.
- **Response time limits (Nielsen).** About 0.1 s feels instant, about 1 s keeps the flow of thought, and about 10 s is the limit of attention. Doherty threshold: keep system response under about 0.4 s so people stay in flow. Show immediate feedback, and avoid animation that delays the result of frequent actions.
- **Serial position effect.** People remember the first and last items in a list best, so place key items there.

## How to apply

- Don't stack all ten on every screen. Pick the heuristics that matter for the screen's job, and name which ones a change addresses.
- A heuristic violation is a hypothesis, not proof. If you can test with real people, test.
