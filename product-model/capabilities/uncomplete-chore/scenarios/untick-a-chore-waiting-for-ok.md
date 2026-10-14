---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps their Chore that is Waiting for OK and confirms
  kind: actor
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product removes the tick; parents have nothing to approve
  kind: product
  actor: kid
  entities:
  - {entity: chore-completion, effect: removes, from: Waiting for OK}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A kid unticks a chore waiting for an OK

## Trigger

A kid ticked the wrong chore.

## Outcome

The chore is open again.

## Edge cases

- A balance can go below zero this way; new purchases wait until it is back up.
