---
kind: primary
result: achieved
routes:
  web: Web
steps:
- text: The Parent taps Connect Google and signs in to Google
  kind: actor
  actor: parent
  capability: connect-calendar-account
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product saves the Calendar account and opens Calendars for that account
  kind: product
  actor: parent
  capability: connect-calendar-account
  entities:
  - {entity: calendar-account, effect: creates, facts: [Provider, Account]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Parent picks members for a calendar and taps Add calendar
  kind: actor
  actor: parent
  capability: add-calendar
  entities:
  - {entity: calendar-account, effect: reads, facts: [Provider, Account]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product adds the Calendar, first in line for the next sync
  kind: product
  actor: parent
  capability: add-calendar
  entities:
  - {entity: calendar, effect: creates, facts: [Name, Kind, Color, Members, Default category, Filter, Enabled, Wall screens and kids' devices can edit,
      Writable]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Connect Google and add its calendar

## Trigger

A parent wants their work calendar on the wall.

## Outcome

The calendar's events show on every screen in the parent's color.
