---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks members for a calendar under Calendars for the account and taps Add calendar
  kind: actor
  actor: parent
  entities:
  - {entity: calendar-account, effect: reads, facts: [Provider, Account]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product adds the Calendar from that Calendar account, first in line for the next sync
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: creates, facts: [Name, Kind, Color, Members, Default category, Filter, Enabled, Wall screens and kids' devices can edit,
      Writable]}
  - {entity: calendar-account, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Add a calendar from a connected account

## Trigger

A parent connected Google and wants their calendar shown.

## Outcome

The calendar syncs both ways, tagged with the picked members.
