---
kind: primary
routes:
  web: Web
steps:
- text: A synced calendar has not synced for the sync interval
  kind: condition
  unattended: true
  entities:
  - {entity: calendar, effect: reads, facts: [Last synced, Enabled]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product syncs the stalest calendars first and keeps only what changed
  kind: product
  entities:
  - {entity: calendar, effect: changes, facts: [Last synced, Sync status]}
  - {entity: event, effect: changes, facts: [Title, Starts, Ends, All day, Location, Notes, Repeat, Reminder, Show as]}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Calendars sync on their own

## Trigger

Time passes.

## Outcome

Every enabled synced calendar stays current without anyone asking.
