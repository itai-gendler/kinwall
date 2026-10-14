---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Done shopping at the end of a trip at a store
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product takes the ticked items off and remembers that store as where they were last bought
  kind: product
  actor: parent
  entities:
  - {entity: list-item, effect: removes, from: Checked off}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Finish a shopping trip

## Trigger

A parent leaves the store.

## Outcome

The bought items are off the list.

## Edge cases

- On a kid's device only the items it may change are cleared.
