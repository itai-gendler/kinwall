---
kind: primary
routes:
  web: Web
steps:
- text: The Kid opens Chores on their own device
  kind: actor
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The device belongs to the Kid, so Chores shows the Kid and Anyone
  kind: condition
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: [Title, Points, Assigned to]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A kid's device shows their own chores

## Trigger

A kid checks their tablet after school.

## Outcome

The kid sees their own chores and the ones for anyone.
