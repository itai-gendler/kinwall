---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps + CalDAV and enters the server, user name and an app-specific password
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product checks the sign-in, saves the Calendar account and opens its calendars to pick from
  kind: product
  actor: parent
  entities:
  - {entity: calendar-account, effect: creates, facts: [Provider, Account]}
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# Connect an iCloud or CalDAV account

## Trigger

A parent keeps the family calendar in iCloud.

## Outcome

The CalDAV account is connected and its calendars are listed.
