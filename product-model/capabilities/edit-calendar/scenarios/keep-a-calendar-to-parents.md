---
kind: primary
routes:
  web: Web
steps:
- text: The Parent turns off Wall screens and kids' devices can edit
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Wall screens and kids' devices can edit]}
  - {entity: wall-screen, effect: reads, facts: []}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
- text: The Product saves it; wall screens and kids' devices now show its events read-only
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: changes, facts: [Wall screens and kids' devices can edit]}
  - {entity: wall-screen, effect: reads, facts: []}
  - {entity: event, effect: reads, facts: []}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
---

# Keep a calendar's events to parents' devices

## Trigger

A parent does not want the work calendar changed from the wall.

## Outcome

Only parents' devices change that calendar's events.

## Edge cases

- Read-only calendars do not show the switch; they say they are read-only.
