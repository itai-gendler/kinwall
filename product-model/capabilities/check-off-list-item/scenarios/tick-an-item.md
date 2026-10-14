---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps an item's circle in the store
  kind: actor
  actor: parent
  entities:
  - {entity: list-item, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product ticks the List item off and notes who checked it off
  kind: product
  actor: parent
  entities:
  - {entity: list-item, effect: changes, from: Open, to: Checked off, facts: [Checked off by, On sale, Steps]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Tick an item off

## Trigger

A parent puts milk in the cart.

## Outcome

The item is crossed off on every screen.

## Edge cases

- Offline, the tick shows at once and is sent when the phone is back online; the last change to reach Kinwall wins.
