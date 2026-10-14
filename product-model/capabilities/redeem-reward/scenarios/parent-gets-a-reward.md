---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Get it on a Reward for a kid
  kind: actor
  actor: parent
  entities:
  - {entity: reward, effect: reads, facts: [Name, Points]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product takes the points and approves the Reward request straight away
  kind: product
  actor: parent
  entities:
  - {entity: reward-request, effect: creates, to: Approved, facts: [Points, Shares, Requested]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# A parent gets a reward for a kid

## Trigger

A parent redeems on a kid's behalf.

## Outcome

The reward is approved and waits to be handed over.
