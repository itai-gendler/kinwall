---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps View on Security activity
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Parent reads each Security activity entry by day, searching it or narrowing it by kind
  kind: actor
  actor: parent
  entities:
  - {entity: security-activity-entry, effect: reads, facts: [What happened, Who did it, Device, When]}
  contexts:
    web: {place: 'web-app::administration::security-activity'}
---

# Read the security log

## Trigger

A parent wants to know who signed in or paired a device.

## Outcome

The parent sees what happened, who did it and when, back a year.
