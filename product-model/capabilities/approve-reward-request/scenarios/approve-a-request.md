---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Approve on a Reward request
  kind: actor
  actor: parent
  entities:
  - {entity: reward-request, effect: reads, facts: [Points, Shares, Requested]}
  contexts:
    web: {place: 'web-app::family::rewards'}
- text: The Product approves it; the points stay spent
  kind: product
  actor: parent
  entities:
  - {entity: reward-request, effect: changes, from: Waiting for OK, to: Approved, facts: []}
  contexts:
    web: {place: 'web-app::family::rewards'}
---

# Approve a request

## Trigger

A parent agrees to ice cream.

## Outcome

The request shows Approved! Coming soon until it is handed over.
