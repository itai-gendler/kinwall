---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Given on an approved Reward request
  kind: actor
  actor: parent
  entities:
  - {entity: reward-request, effect: reads, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product marks it given
  kind: product
  actor: parent
  entities:
  - {entity: reward-request, effect: changes, from: Approved, to: Given, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Mark a reward given

## Trigger

The ice cream was had.

## Outcome

The request moves to Recent as Given.
