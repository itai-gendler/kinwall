---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Use a security key or another device and confirms on the key or the nearby phone
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product saves the Passkey, labeled Security key
  kind: product
  actor: parent
  entities:
  - {entity: passkey, effect: creates, facts: [Name, Whose device, Added]}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Add a security key or another device

## Trigger

A parent wants a hardware key as a second way in.

## Outcome

The security key signs a parent in from now on.

## Edge cases

- Passkeys need https or localhost; on a plain IP address Kinwall offers recovery codes or an admin key instead.
