# Forms and feedback

For layout and flow questions (which fields, steps, order), see `ux/references/forms.md`. This file covers what makes forms work with assistive technology.

## Labels and instructions

- Every input has a **visible `<label>` associated with it** (`for`/`id`, or wrapping). A placeholder is not a label.
- Group related controls (radio buttons, checkboxes, address parts) in a `<fieldset>` with a `<legend>`.
- Put format hints and requirements in text linked with `aria-describedby`, visible before the person types.
- Mark required fields in text ("required" or an asterisk explained) and use the `required` attribute. Mark optional ones in text when most are required.
- Use the right `type` and `autocomplete` values (`email`, `tel`, `given-name`, `postal-code`, `new-password`, and so on) to reduce typing and help people with cognitive or motor disabilities.
- Do not block paste into password or confirmation fields.

## Errors

- Identify the field in error and **describe the problem and the fix in text**. Color or an icon alone is not enough.
- Connect the message to the field with `aria-describedby`, and set `aria-invalid="true"` on the invalid field.
- On a failed submit, move focus to the first error or to a summary at the top with links to each field, and announce it (for example `role="alert"` on the summary).
- Keep what the person typed.
- Do not rely on `title` attributes or the browser's native bubble alone for errors.
- For legal, financial or data-changing submissions, let people review, correct or undo before it is final.
- Don't ask again for information the person already entered in the same flow (WCAG 2.2 redundant entry).
- Provide an accessible way to authenticate: no cognitive tests such as memorizing or transcribing codes as the only option, and allow password managers and paste.

## Status messages and loading

- Announce changes that do not move focus (saved, item added, results loaded, error) with a polite live region (`role="status"`). Use `role="alert"` only for urgent, time-sensitive problems.
- The live region must be in the DOM before its text changes, and its messages should be short.
- Loading states: expose busy content (`aria-busy="true"` on the region), show visible text or a labeled spinner, and announce completion.
- A disabled submit button hides the reason from many people. Prefer an enabled button that explains what is missing on submit.
- Toasts that disappear must stay long enough to read, be pausable, and not be the only place essential information appears.

## Authentication and timeouts

- Warn before a session expires and let people extend it without losing their work.
- Allow password managers and avoid blocking copy and paste.
