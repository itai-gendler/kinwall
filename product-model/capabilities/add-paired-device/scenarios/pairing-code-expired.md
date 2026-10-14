---
kind: validation
routes:
  web: Web
steps:
- text: The Parent enters a code and taps Add it
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::access'}
- text: No screen is waiting with that code, or its 10 minutes are up
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product says the code was not found or expired
  kind: product
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::access'}
---

# An unknown or expired pairing code is refused

## Trigger

A parent types a code after it ran out.

## Outcome

Nothing is paired; the screen can show a new code.
