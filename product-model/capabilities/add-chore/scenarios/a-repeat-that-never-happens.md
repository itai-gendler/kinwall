---
kind: validation
routes:
  web: Web
steps:
- text: The Parent gives a chore a repeat such as the 30th of February
  kind: actor
  actor: parent
  entities:
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The repeat never happens
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product says "That repeat never happens. Check the day and month." and adds nothing
  kind: product
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A repeat that never happens is refused

## Trigger

A parent picks an impossible repeat.

## Outcome

No chore is added.

## Edge cases

- A repeat more often than daily, such as hourly, is refused too.
