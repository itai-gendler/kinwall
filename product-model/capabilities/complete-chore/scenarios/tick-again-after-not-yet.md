---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps a Chore that shows "Not yet" with a parent's note
  kind: actor
  actor: kid
  entities:
  - {entity: chore-completion, effect: reads, facts: [Not yet note]}
  - {entity: parent, effect: reads, facts: []}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product clears the note and the tick waits for a parent's OK again
  kind: product
  actor: kid
  entities:
  - {entity: chore-completion, effect: changes, from: Not yet, to: Waiting for OK, facts: [Ticked at, Not yet note]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Tick a chore again after Not yet

## Trigger

A kid made the bed properly this time.

## Outcome

The chore waits for an OK once more.
