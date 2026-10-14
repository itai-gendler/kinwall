---
kind: primary
routes:
  web: Web
steps:
- text: The Kid reads the answer on a Chore idea and taps Got it
  kind: actor
  actor: kid
  entities:
  - {entity: chore-idea, effect: reads, facts: [Title, Note]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product puts the card away
  kind: product
  actor: kid
  entities:
  - {entity: chore-idea, effect: changes, from: Approved, to: Put away, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Put away an answer

## Trigger

A kid has read that their idea was approved.

## Outcome

The card no longer shows under Chore ideas.

## Edge cases

- An idea a grown-up said Not this time to is put away the same way.
