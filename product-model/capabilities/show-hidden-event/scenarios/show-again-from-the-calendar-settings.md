---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens Hidden events in Edit calendar and taps Show again on an Event
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title, Starts]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
- text: The Product shows it, or its series, to the family again
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, from: Hidden, to: Shown, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
---

# Show an event again from Hidden events

## Trigger

A parent reviews what was hidden on a calendar.

## Outcome

The event shows again.
