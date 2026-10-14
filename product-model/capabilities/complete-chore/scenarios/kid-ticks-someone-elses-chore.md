---
kind: validation
routes:
  web: Web
steps:
- text: The Kid ticks a sibling's Chore through a link
  kind: actor
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: [Title, Assigned to]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Chore belongs to someone else
  kind: condition
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product says this device can only do that for the Kid
  kind: product
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A kid's device cannot tick someone else's chore

## Trigger

A kid tries to tick their sister's chore.

## Outcome

Nothing is ticked.
