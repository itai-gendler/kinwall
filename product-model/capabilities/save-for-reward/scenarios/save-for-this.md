---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps Save for this on a Reward
  kind: actor
  actor: kid
  entities:
  - {entity: reward, effect: reads, facts: [Name, Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product makes it the Kid's goal
  kind: product
  actor: kid
  entities:
  - {entity: family-member, effect: changes, facts: [Reward goal]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Save for a reward

## Trigger

A kid wants the big reward.

## Outcome

The Board shows "🍿 Movie night pick 40 / 100" on the kid's row, and Ready! once they have enough.
