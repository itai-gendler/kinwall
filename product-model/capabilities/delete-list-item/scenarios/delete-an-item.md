---
kind: primary
routes:
  web: Web
steps:
- text: The Parent swipes a List item left and taps Delete
  kind: actor
  actor: parent
  entities:
  - {entity: list-item, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product deletes it and offers Undo for a few seconds
  kind: product
  actor: parent
  entities:
  - {entity: list-item, effect: removes, from: Open}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Delete an item

## Trigger

An item is not needed.

## Outcome

The item is gone; Undo brings it back exactly as it was.
