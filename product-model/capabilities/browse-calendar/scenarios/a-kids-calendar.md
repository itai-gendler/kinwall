---
kind: primary
routes:
  web: Web
steps:
- text: The Kid opens Calendar on their own device
  kind: actor
  actor: kid
  entities:
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: The device belongs to the Kid, so the calendar keeps to their events
  kind: condition
  actor: kid
  entities:
  - {entity: event, effect: reads, facts: [Title, Starts, Who]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
---

# A kid's device shows their own events

## Trigger

A kid checks what is on.

## Outcome

The kid sees their own events.
