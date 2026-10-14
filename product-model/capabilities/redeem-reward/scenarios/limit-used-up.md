---
kind: validation
routes:
  web: Web
steps:
- text: The Kid tries to get a limited Reward again
  kind: actor
  actor: kid
  entities:
  - {entity: reward, effect: reads, facts: [Limit]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Kid already used its limit for today or this week
  kind: condition
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product says "That's all for today" and takes nothing
  kind: product
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# A reward's limit is used up

## Trigger

A kid wants a fourth round of screen time.

## Outcome

Nothing is spent until the next day or week.
