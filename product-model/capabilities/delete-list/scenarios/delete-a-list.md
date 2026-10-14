---
kind: primary
routes:
  web: Web
steps:
- text: The Parent deletes a List and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product deletes it with all its items
  kind: product
  actor: parent
  entities:
  - {entity: list, effect: removes, from: Active}
  - {entity: list-item, effect: removes, from: Open, with: list}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Delete a list

## Trigger

A list is no longer needed.

## Outcome

The list and its items are gone.
