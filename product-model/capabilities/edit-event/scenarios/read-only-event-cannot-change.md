---
kind: validation
routes:
  web: Web
steps:
- text: The Parent opens an Event from an ICS feed
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Calendar is read-only
  kind: condition
  entities:
  - {entity: calendar, effect: reads, facts: [Writable]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product offers no Edit; only people, category and travel time can be set
  kind: product
  actor: parent
  entities:
  - {entity: category, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# A read-only event's details cannot change

## Trigger

A parent wants to change a school event.

## Outcome

The event stays as the feed says.
