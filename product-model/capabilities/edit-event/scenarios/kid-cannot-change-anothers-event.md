---
kind: validation
routes:
  web: Web
steps:
- text: The Kid opens an Event on the family calendar
  kind: actor
  actor: kid
  entities:
  - {entity: event, effect: reads, facts: [Title]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Calendar is not one of the Kid's
  kind: condition
  actor: kid
  entities:
  - {entity: calendar, effect: reads, facts: [Members]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product opens the event read-only, saying this device can't change events on that calendar
  kind: product
  actor: kid
  entities:
  - {entity: calendar, effect: reads, facts: []}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# A kid's device cannot change someone else's calendar

## Trigger

A kid tries to move a family event.

## Outcome

The event is unchanged.
