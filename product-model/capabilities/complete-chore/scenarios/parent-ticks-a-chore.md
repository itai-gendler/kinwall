---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps a Chore on today's column
  kind: actor
  actor: parent
  entities:
  - {entity: chore, effect: reads, facts: [Title, Points, Assigned to]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product marks it done for today and credits its points to the chore's person
  kind: product
  actor: parent
  entities:
  - {entity: chore-completion, effect: creates, to: Done, facts: [Day, Done by, Points earned, Ticked at]}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A parent ticks a chore off

## Trigger

A parent saw the dishes done.

## Outcome

The chore is done and the points count at once.
