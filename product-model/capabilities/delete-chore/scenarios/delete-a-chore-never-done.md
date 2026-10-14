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
- text: Nobody ever completed the Chore
  kind: condition
  entities:
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product removes it completely
  kind: product
  actor: parent
  entities:
  - {entity: chore, effect: removes, from: Active}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Delete a chore that was never done

## Trigger

A chore was added by mistake.

## Outcome

The chore is gone.
