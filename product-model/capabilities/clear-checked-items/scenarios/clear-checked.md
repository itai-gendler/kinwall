---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Clear checked
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product removes the ticked items and says "Cleared 5 items" with Undo
  kind: product
  actor: parent
  entities:
  - {entity: list-item, effect: removes, from: Checked off}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Clear checked items

## Trigger

The shopping is put away.

## Outcome

Only open items are left.
