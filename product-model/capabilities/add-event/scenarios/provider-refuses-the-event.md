---
kind: edge
routes:
  web: Web
steps:
- text: The Parent adds an event to a Google Calendar
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Name, Kind]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: Google refuses or cannot be reached
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: The Product stores nothing and says it couldn't be saved to the calendar
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
---

# The provider refuses the new event

## Trigger

Google is down.

## Outcome

No event is added anywhere.
