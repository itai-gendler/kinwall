---
kind: primary
routes:
  web: Web
steps:
- text: The Kid adds "Library books" to a to-do List and assigns it to themselves
  kind: actor
  actor: kid
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product adds the List item, added by the Kid
  kind: product
  actor: kid
  entities:
  - {entity: list-item, effect: creates, to: Open, facts: [Title, Quantity, Store, Aisle, Department, For, Assign to, Added by]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# A kid adds a to-do for themselves

## Trigger

A kid needs to return books.

## Outcome

The to-do shows the kid as its owner.

## Edge cases

- A kid's own device can assign an item to itself or to nobody, never to someone else.
