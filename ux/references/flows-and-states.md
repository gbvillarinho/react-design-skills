# Flows and states

A screen is not one picture. It is a set of states, and people spend a lot of time in the ones designers skip.

## The five states every screen needs

| State | What to design |
|---|---|
| **Empty** | Say what belongs here and offer the action that fills it. An empty screen is an invitation, not a dead end. |
| **Loading** | Show that something is happening. Use skeletons that match the final layout for content, and spinners only for short waits. For long waits, show progress or an estimate. |
| **Partial** | Some data, some failure, or only a few items. Make sure the layout still works and nothing misleading appears. |
| **Error** | Say what went wrong and how to fix it, keep the person's input, and offer a way to retry. |
| **Success** | Confirm what happened using the same name as the action, and show the next step. |

Also consider: offline, no permission, very long content, very large lists, and first-time versus returning users.

## Flows

- **Shorten the path.** Count the steps and fields between the person and their goal. Remove, combine or default them.
- **Show progress** in multi-step flows (where you are, how many steps remain), and let people go back without losing their work.
- **Ask for information when it is needed**, not before. Let people see value first, then ask for signup or details.
- **Onboarding** teaches by doing. Prefer getting the person to their first success over a tour of features. Make it skippable.
- **Save work automatically** where possible, and say that it was saved.

## Destructive and irreversible actions

- Prefer **undo** over "Are you sure?". Confirmation dialogs are habitually clicked through, while undo actually protects.
- When confirmation is needed (permanent deletion, payment, sending to many people), **name the consequence** in the dialog and label the button with the action ("Delete project"), not "OK".
- Keep destructive actions visually and spatially apart from safe ones.

## Feedback

- Every action gets a response: visual change, message or state change, within about a second.
- Keep messages near where the action happened. Use toasts for low-stakes confirmations, and inline messages for anything the person must act on.
- Don't rely on color alone to communicate state.

## Navigation

- Mark the current location, and keep navigation in the same place everywhere.
- Name items by the person's goal, not the system's structure.
- Offer a visible way back and a way home.
