---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks the default calendar and the default length
  kind: actor
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: [Default calendar for new events, New events last]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product saves them; new events start on that calendar with that length
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Default calendar for new events, New events last]}
  - {entity: calendar, effect: reads, facts: []}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Pick the default calendar and event length

## Trigger

New events keep going to the wrong calendar.

## Outcome

New events go to the picked calendar.

## Edge cases

- A picked calendar that is removed, turned off or becomes read-only falls back to Automatic.
