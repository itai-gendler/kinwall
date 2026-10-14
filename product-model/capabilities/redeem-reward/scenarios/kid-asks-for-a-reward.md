---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps Get it on a Reward and confirms "Spend 50 points on 🍦 Ice cream trip? Leo will have 20 left."
  kind: actor
  actor: kid
  entities:
  - {entity: reward, effect: reads, facts: [Name, Points]}
  - {entity: family-member, effect: reads, facts: [Points to spend]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product takes the points and saves the Reward request as Waiting for OK, telling parents' devices
  kind: product
  actor: kid
  entities:
  - {entity: reward-request, effect: creates, to: Waiting for OK, facts: [Points, Shares, Requested]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# A kid gets a reward that needs an OK

## Trigger

A kid has saved enough for ice cream.

## Outcome

The request shows under Waiting for a grown-up; the points are set aside.
