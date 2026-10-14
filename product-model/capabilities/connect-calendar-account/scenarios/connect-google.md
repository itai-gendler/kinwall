---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Connect Google
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Parent signs in to Google and allows Kinwall to see and change their calendars
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product saves the Calendar account and opens its calendars to pick from
  kind: product
  actor: parent
  entities:
  - {entity: calendar-account, effect: creates, facts: [Provider, Account]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Connect Google

## Trigger

A parent wants their Google calendar on the wall.

## Outcome

The Google account is connected and its calendars are listed under Calendars for that account.

## Edge cases

- Connect Outlook works the same way with a Microsoft account.
- Reconnect on a calendar Google stopped letting Kinwall see starts the same sign-in; its calendars sync again with their settings kept.
