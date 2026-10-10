# Showing data

A chart is an answer to a question. Before drawing anything, write the question the person is asking ("Which stores are behind target, and by how much?"), then choose the form that answers it. For any chart, bar, KPI or number-heavy table, also read the `dataviz` skill for palette, marks, labels and interaction details.

## Choose the form by the question

| Question | Use | Avoid |
|---|---|---|
| How is this against a target? | A bullet chart, or a bar on a shared scale with the target marked and labeled | A filled progress bar with no visible scale or target |
| Which items rank highest or lowest? | Sorted horizontal bars on one common baseline, value labeled at the end | Bars scaled to the top item with decorative color |
| How is it changing over time? | A line with a labeled axis, a reference (previous period, target) and the latest value marked | A tiny unlabeled sparkline used as decoration |
| What share of a whole is each part? | Stacked bar or a few labeled segments, only when parts add up to a whole | A pie with many slices |
| How do two things relate? | Scatter plot with labeled outliers | Two separate charts the reader must compare by eye |
| I need exact values | A table, aligned right, with units in the header | A chart that forces guessing |

## Rules

- **Every number needs a comparison.** A KPI alone says nothing. Show it against a target, the previous period or a range, and say which direction is good.
- **Same scale for things that are compared.** Bars in one group share one axis. If a scale starts above zero, say so.
- **Label directly.** Put values and the target mark on the chart, so the reader does not need a legend or a decoder.
- **Color carries meaning.** Use one neutral color for ordinary data and a second only for what needs attention (behind target). Do not color bars for variety.
- **Redundant encoding adds noise.** If the value is printed next to the bar and the bar only restates it, make the bar earn its place by showing a comparison.
- **Check the numbers.** Percent changes, projections and targets must follow from the data shown. Do not hardcode figures that cannot be derived from it.
- **Honest rules for derived metrics.** If a metric needs a definition (pace to date, projection), show the result in plain words and move the formula to a short hint.

## Titles and text on data

- The title states the finding or the question: "3 stores are behind target", not "Stores below target".
- The subtitle gives period, unit and source in a short line.
- Keep formulas and methodology out of the main view; put them behind a hint or note.

## Dashboard layout

- Lead with the answer to the main question, then the detail that explains it.
- Avoid stacking identical dark cards with borders. Group by the question being answered, and let size and position show importance.
- Give each block one job, and remove blocks that do not change a decision.
