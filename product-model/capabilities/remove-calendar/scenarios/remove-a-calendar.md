---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Remove on a Calendar and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product removes the Calendar and its events from Kinwall
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: removes}
  - {entity: event, effect: removes, from: Shown, with: calendar}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Remove a calendar

## Trigger

A family stops using a calendar.

## Outcome

Its events are gone from every screen; the original calendar is untouched.
