---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Add a passkey on this phone or computer and confirms with the device's screen lock
  kind: actor
  actor: parent
  entities:
  - {entity: passkey, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product saves the Passkey for this device
  kind: product
  actor: parent
  entities:
  - {entity: passkey, effect: creates, facts: [Name, Whose device, Added]}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Add a passkey on this device

## Trigger

A parent wants to sign in on this device without a key.

## Outcome

The passkey is listed under Parent devices and works for later sign-ins.
