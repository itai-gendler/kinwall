---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Sync now on a synced Calendar
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Name, Last synced]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product fetches the calendar's events and keeps only what changed
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: changes, facts: [Last synced, Sync status]}
  - {entity: event, effect: changes, facts: [Title, Starts, Ends, All day, Location, Notes, Repeat, Reminder, Show as]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Sync a calendar now

## Trigger

A parent just added something in Google.

## Outcome

The new event shows in Kinwall and the row says when it synced.
