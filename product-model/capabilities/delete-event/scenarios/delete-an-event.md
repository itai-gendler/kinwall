---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens an Event, taps Delete and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product deletes it, from the provider first on a synced calendar
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: removes, from: Shown}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Delete an event

## Trigger

A party is cancelled.

## Outcome

The event is gone from Kinwall and from the original calendar.
