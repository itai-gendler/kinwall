---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps + Local calendar and enters a name
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product adds a writable Calendar kept only in Kinwall, in the next unused color
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: creates, facts: [Name, Kind, Color, Members, Default category, Filter, Enabled, Wall screens and kids' devices can edit,
      Writable]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Add a Kinwall-only calendar

## Trigger

A family wants a calendar that lives only in Kinwall.

## Outcome

The calendar is ready for events.
