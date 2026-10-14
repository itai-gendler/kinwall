---
kind: validation
routes:
  web: Web
steps:
- text: The Wall screen adds an event to a Calendar
  kind: actor
  actor: wall-screen
  entities:
  - {entity: calendar, effect: reads, facts: [Wall screens and kids' devices can edit]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: Wall screens and kids' devices can edit is off for that calendar
  kind: condition
  entities:
  - {entity: wall-screen, effect: reads, facts: []}
  - {entity: calendar, effect: reads, facts: []}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: The Product says events on this calendar can only be changed from a parent's device
  kind: product
  actor: wall-screen
  entities:
  - {entity: calendar, effect: reads, facts: []}
  - {entity: parent, effect: reads, facts: []}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
---

# A wall screen cannot add to a parents-only calendar

## Trigger

Someone at the wall tries to add to the work calendar.

## Outcome

Nothing is added.
