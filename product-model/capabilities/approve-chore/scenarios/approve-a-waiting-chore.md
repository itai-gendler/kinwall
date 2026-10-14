---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Approve on a Chore completion under To approve
  kind: actor
  actor: parent
  entities:
  - {entity: chore-completion, effect: reads, facts: [Day, Done by, Ticked at]}
  - {entity: chore, effect: reads, facts: [Title, Points]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product marks it done and awards its points, judged by when it was ticked
  kind: product
  actor: parent
  entities:
  - {entity: chore-completion, effect: changes, from: Waiting for OK, to: Done, facts: [Points earned]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Approve a waiting chore

## Trigger

A parent checks the bed is made.

## Outcome

The kid gets the points; ticked on its day, it earns in full even approved the next morning.

## Edge cases

- Two parents approving at once award the points once.
