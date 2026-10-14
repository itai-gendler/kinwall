---
kind: validation
routes:
  web: Web
steps:
- text: The Kid tries to get a Reward
  kind: actor
  actor: kid
  entities:
  - {entity: reward, effect: reads, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Kid has fewer points to spend than it costs
  kind: condition
  actor: kid
  entities:
  - {entity: family-member, effect: reads, facts: [Points to spend]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product shows how many more points it needs and takes nothing
  kind: product
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Not enough points

## Trigger

A kid is short of points.

## Outcome

Nothing is spent.
