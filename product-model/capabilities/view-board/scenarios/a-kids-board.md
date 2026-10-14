---
kind: primary
routes:
  web: Web
steps:
- text: The Kid opens Home on their own device
  kind: actor
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::home'}
- text: The device belongs to the Kid, so the Board keeps to their events, chores and lists
  kind: condition
  actor: kid
  entities:
  - {entity: event, effect: reads, facts: [Title, Starts, Who]}
  - {entity: chore, effect: reads, facts: [Title, Points]}
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::home'}
---

# A kid's device shows their own Board

## Trigger

A kid checks their own tablet.

## Outcome

The kid sees only their own day.
