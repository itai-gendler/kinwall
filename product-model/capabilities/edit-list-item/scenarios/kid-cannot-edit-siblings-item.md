---
kind: validation
routes:
  web: Web
steps:
- text: The Kid taps a sibling's List item
  kind: actor
  actor: kid
  entities:
  - {entity: list-item, effect: reads, facts: [Title, Assign to]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The item belongs to someone else on a list that is not the Kid's
  kind: condition
  actor: kid
  entities:
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product opens it to read only, saying whose it is
  kind: product
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::list'}
---

# A kid's device cannot change a sibling's item

## Trigger

A kid opens their sister's to-do.

## Outcome

The item is unchanged.
