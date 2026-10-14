---
kind: edge
routes:
  web: Web
steps:
- text: The Parent taps Sync now
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The provider or feed cannot be reached or turns Kinwall down
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product keeps the events it had and shows the error in plain words on the calendar's row
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: changes, facts: [Sync status]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# A sync fails

## Trigger

A feed is down.

## Outcome

The family still sees the last events; the row says what went wrong.

## Edge cases

- When Google or Outlook stops letting Kinwall see a calendar, the row asks to Reconnect.
