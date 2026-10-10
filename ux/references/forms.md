# Forms

Forms are where people give up. Every field and every unclear error costs completions.

## Fewer fields

- Ask only for what you need now. For each field, ask what breaks if you remove it.
- Use sensible defaults, autofill and the right input types (email, number, date, telephone) so mobile shows the right keyboard.
- Split long forms into short, labeled steps, with progress shown.

## Layout

- **One column.** It is faster to scan and avoids missed fields.
- **Labels above fields**, always visible. Placeholders disappear when typing, so don't use them as labels. Use them for examples only.
- **Group related fields** with space and headings (shipping vs. billing).
- **Mark optional fields** rather than every required one, when most are required.
- Make field width hint at the expected input (a short field for a postal code).
- Put the primary button after the last field, aligned with the fields, with a specific label ("Create account", not "Submit").

## Validation and errors

- **Validate when the person leaves the field**, not on every keystroke. Exceptions: password rules and character counters, which help while typing.
- Show the error **next to the field**, and summarize at the top if the form is long, with links to each problem.
- **Say how to fix it:** "Enter a date like 24/03/2026", not "Invalid input". Don't blame the person.
- **Keep what they typed.** Never clear the form on error.
- Don't rely on color alone. Use text and an icon too.
- Move focus to the first error after a failed submit.

## Interaction details

- Let people see passwords, and paste into any field.
- Don't make people retype something you already know (email in a confirmation field, billing equal to shipping).
- Disable a submit button only if you tell people why. Otherwise, let them submit and explain what is missing.
- Show a clear loading state on submit, and prevent double submission.
- Confirm success with what happened and what comes next.

## Choosing input types

| Situation | Use |
|---|---|
| 2 to 5 mutually exclusive options | Radio buttons, all visible |
| Many options | Select or searchable list |
| Yes or no | Checkbox, or a switch if it takes effect immediately |
| Picking a number in a range | Slider with a visible value, or a number input for precision |
| Dates | Native date input, or separate day, month and year fields for known dates like birthdays |

## Question the structure before designing it

A brief that lists fields is not a requirement to collect all of them now. Before building, answer these and write the answers down, flagging each business decision for the person to confirm:

- **Which fields does this moment really need?** Account creation usually needs an email and a password (or just an email). Address, tax ID and birth date often belong later, at checkout or when first needed. Offer to move or drop them instead of silently keeping every field.
- **Steps or one page?** With about five fields or fewer, one page is usually faster. Steps help when groups are long or clearly different. If you split, each step should have a reason a person could state ("sign-in details, then delivery").
- **Is the order right?** Start with what the person expects to give first and what is easiest. Put the most sensitive or effortful items last, after they have invested.
- **Who decides?** Collecting data is often a business, legal or product decision. Say so, state your recommendation and the alternative, and let the person choose.
