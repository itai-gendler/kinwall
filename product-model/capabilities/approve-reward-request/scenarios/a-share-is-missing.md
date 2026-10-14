---
kind: edge
routes:
  web: Web
steps:
- text: The Parent taps Approve on a split Reward request
  kind: actor
  actor: parent
  entities:
  - {entity: reward-request, effect: reads, facts: [Shares]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: Someone chipping in spent their points meanwhile
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product says "Leo has only 40 points now, not 100" and changes nothing
  kind: product
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Someone chipping in no longer has their share

## Trigger

A sibling spent their points first.

## Outcome

The request still waits; the parent can say not this time or wait.
