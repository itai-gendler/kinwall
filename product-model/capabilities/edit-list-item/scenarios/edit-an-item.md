---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps a List item and changes its quantity and store
  kind: actor
  actor: parent
  entities:
  - {entity: list-item, effect: reads, facts: [Title, Quantity, Store]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product saves it and remembers the store for that name
  kind: product
  actor: parent
  entities:
  - {entity: list-item, effect: changes, facts: [Quantity, Store]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Edit an item

## Trigger

Two cartons are needed, from another store.

## Outcome

Everyone sees the change.
