---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks More… → Delete chore… and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: chore, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Chore was done before
  kind: condition
  entities:
  - {entity: chore-completion, effect: reads, facts: []}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product takes it off every list and keeps its history and the points earned from it
  kind: product
  actor: parent
  entities:
  - {entity: chore, effect: changes, from: Active, to: Archived, facts: []}
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Delete a chore that was done before

## Trigger

A chore is no longer needed.

## Outcome

It leaves the chart; profiles and points still count it.

## Edge cases

- A tick still waiting for a parent's OK goes with it.
