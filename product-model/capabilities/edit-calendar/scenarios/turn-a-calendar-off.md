---
kind: primary
routes:
  web: Web
steps:
- text: The Parent turns off Enabled
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Enabled]}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
- text: The Product stops syncing the Calendar and hides its events
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: changes, facts: [Enabled]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
---

# Turn a calendar off

## Trigger

A calendar is not needed for a while.

## Outcome

Its events are hidden until it is turned back on.
