---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Undo on "Gave Maya 10 points"
  kind: actor
  actor: parent
  entities:
  - {entity: bonus-points, effect: reads, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product takes the Bonus points back
  kind: product
  actor: parent
  entities:
  - {entity: bonus-points, effect: removes}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Undo bonus points

## Trigger

Points went to the wrong kid.

## Outcome

The points are gone from the balance and totals.
