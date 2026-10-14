---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Cancel on an approved Reward request
  kind: actor
  actor: parent
  entities:
  - {entity: reward-request, effect: reads, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product gives the points back
  kind: product
  actor: parent
  entities:
  - {entity: reward-request, effect: changes, from: Approved, to: Not this time, facts: [Note]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Call off an approved reward

## Trigger

An approved trip falls through.

## Outcome

The points are back.
