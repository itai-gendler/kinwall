---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps + ICS URL and enters the feed link and a name
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product adds a read-only Calendar for the feed, never synced, first in line for the next sync
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: creates, facts: [Name, Kind, Color, Members, Default category, Filter, Enabled, Wall screens and kids' devices can edit,
      Writable, Feed link]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Subscribe to an ICS feed

## Trigger

A school publishes its calendar as a link.

## Outcome

The school's events show on the wall, read-only.
