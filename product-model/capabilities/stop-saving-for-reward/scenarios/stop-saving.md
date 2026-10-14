---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps Stop saving under their goal
  kind: actor
  actor: kid
  entities:
  - {entity: family-member, effect: reads, facts: [Reward goal]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product clears the goal
  kind: product
  actor: kid
  entities:
  - {entity: family-member, effect: changes, facts: [Reward goal]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Stop saving

## Trigger

A kid changes their mind.

## Outcome

No goal shows for them.
