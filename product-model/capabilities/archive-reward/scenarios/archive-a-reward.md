---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Archive on a Reward
  kind: actor
  actor: parent
  entities:
  - {entity: reward, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product hides it from everyone
  kind: product
  actor: parent
  entities:
  - {entity: reward, effect: changes, from: Active, to: Archived, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Archive a reward

## Trigger

A reward is out of season.

## Outcome

Nobody sees it; its history stays.
