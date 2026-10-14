---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps a chip on a repeating synced Event and picks All events in the series
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title, Who, Repeat]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product tags every event in the series
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, facts: [Who]}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Tag someone on a whole synced series

## Trigger

A kid joins a weekly class from the school feed.

## Outcome

Every class shows on the kid's day.

## Edge cases

- A tag on one event wins over the series' tags, which win over the calendar's members.
