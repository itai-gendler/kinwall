---
kind: primary
result: achieved
routes:
  web: Web
steps:
- text: The Kid taps their Bedtime Chore
  kind: actor
  actor: kid
  capability: complete-chore
  entities:
  - {entity: chore, effect: reads, facts: [Title, Checklist]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product opens the checklist in Get stuff done because items are still open
  kind: product
  actor: kid
  capability: complete-chore
  entities:
  - {entity: list-item, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
- text: The Kid ticks off each List item
  kind: actor
  actor: kid
  capability: check-off-list-item
  entities:
  - {entity: list-item, effect: reads, facts: [Title, Steps]}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
- text: The Product ticks each one off for the Kid and says All done!
  kind: product
  actor: kid
  capability: check-off-list-item
  entities:
  - {entity: list-item, effect: changes, from: Open, to: Checked off, facts: [Checked off by, On sale, Steps]}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
- text: The Kid taps Complete Bedtime
  kind: actor
  actor: kid
  capability: complete-chore
  entities:
  - {entity: chore, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::get-stuff-done'}
- text: The Product completes the chore for today
  kind: product
  actor: kid
  capability: complete-chore
  entities:
  - {entity: chore-completion, effect: creates, to: Waiting for OK, facts: [Day, Done by, Points earned, Ticked at]}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Work through the Bedtime checklist

## Trigger

A kid starts their bedtime routine.

## Outcome

The chore waits for a parent's OK, and the reusable checklist resets for tomorrow.
