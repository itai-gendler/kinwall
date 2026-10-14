---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps Cancel request on a Reward request still Waiting for OK and confirms
  kind: actor
  actor: kid
  entities:
  - {entity: reward-request, effect: reads, facts: [Points]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product gives the points back and removes the request
  kind: product
  actor: kid
  entities:
  - {entity: reward-request, effect: removes, from: Waiting for OK}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Cancel a request

## Trigger

A kid changes their mind.

## Outcome

The points are back; the request does not count toward the limit.
