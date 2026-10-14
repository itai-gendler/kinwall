---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Restore on an archived Reward
  kind: actor
  actor: parent
  entities:
  - {entity: reward, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product offers it again
  kind: product
  actor: parent
  entities:
  - {entity: reward, effect: changes, from: Archived, to: Active, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Restore a reward

## Trigger

Summer is back.

## Outcome

The reward is offered again.
