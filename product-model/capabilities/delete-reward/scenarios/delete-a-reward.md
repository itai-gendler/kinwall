---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Delete on a Reward
  kind: actor
  actor: parent
  entities:
  - {entity: reward, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product deletes it and clears it as anyone's goal
  kind: product
  actor: parent
  entities:
  - {entity: reward, effect: removes, from: Active}
  - {entity: family-member, effect: changes, facts: [Reward goal]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Delete a reward

## Trigger

A reward will not be offered again.

## Outcome

It is gone; past requests still show in history.
