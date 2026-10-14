---
kind: validation
routes:
  web: Web
steps:
- text: The Parent enters a feed link
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The link is not a public web address Kinwall can read
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
- text: The Product says the link can't be used and adds nothing
  kind: product
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::calendars'}
---

# A feed link Kinwall cannot use is refused

## Trigger

A parent pastes a local address.

## Outcome

No calendar is added.
