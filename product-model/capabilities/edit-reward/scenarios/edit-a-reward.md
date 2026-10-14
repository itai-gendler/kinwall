---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps a Reward in Manage rewards and changes its points
  kind: actor
  actor: parent
  entities:
  - {entity: reward, effect: reads, facts: [Name, Emoji, Points, For, Needs a parent's OK, Limit]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product saves it; past requests keep their price
  kind: product
  actor: parent
  entities:
  - {entity: reward, effect: changes, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Edit a reward

## Trigger

A reward is too cheap.

## Outcome

It costs the new points from now on.
