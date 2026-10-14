---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps a List item, then Move to another list…, and picks a List of the same type
  kind: actor
  actor: parent
  entities:
  - {entity: list-item, effect: reads, facts: [Title]}
  - {entity: list, effect: reads, facts: [Name, Type]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product moves the item to the end of that list with everything on it
  kind: product
  actor: parent
  entities:
  - {entity: list-item, effect: changes, facts: []}
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Move an item to another list

## Trigger

Paint belongs on the hardware store list.

## Outcome

The item is on the other list.
