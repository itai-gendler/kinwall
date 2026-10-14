---
kind: primary
routes:
  web: Web
steps:
- text: The Kid opens Rewards on their own device
  kind: actor
  actor: kid
  entities:
  - {entity: reward, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Kid reads their points, their goal, each Reward they can get now or keep saving for, and their requests
  kind: actor
  actor: kid
  entities:
  - {entity: family-member, effect: reads, facts: [Name, Points to spend, Reward goal]}
  - {entity: reward, effect: reads, facts: [Name, Emoji, Points, Limit]}
  - {entity: reward-request, effect: reads, facts: [Points, Note, Requested]}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Look at a kid's rewards

## Trigger

A kid wonders what they can get.

## Outcome

The kid sees what is ready, how far the rest are, and what is waiting.

## Edge cases

- A shared wall screen never shows requests a parent said not this time to.
