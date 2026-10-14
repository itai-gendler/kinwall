---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps a done Chore and confirms Mark "…" not done?
  kind: actor
  actor: wall-screen
  entities:
  - {entity: chore, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product removes the tick and its points
  kind: product
  actor: wall-screen
  entities:
  - {entity: chore-completion, effect: removes, from: Done}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Mark a chore not done

## Trigger

A chore was ticked by mistake.

## Outcome

The chore is open again and its points are gone from the balance.
