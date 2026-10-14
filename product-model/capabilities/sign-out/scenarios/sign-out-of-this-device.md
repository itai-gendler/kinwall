---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Sign out under Parent devices
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product ends this device's passkey session
  kind: product
  actor: parent
  entities:
  - {entity: passkey, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Sign out of this device

## Trigger

A parent is done with a borrowed computer.

## Outcome

The device is signed out and shows the sign-in screen next time.
