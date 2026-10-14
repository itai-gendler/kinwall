---
kind: primary
routes:
  web: Web
steps:
- text: The Parent chooses Sign in as a parent and confirms with Face ID, Touch ID, the screen lock or a security key
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
- text: The Product checks the Passkey and starts a 30-day parent session on this device
  kind: product
  actor: parent
  entities:
  - {entity: passkey, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
---

# Sign in with a passkey

## Trigger

A parent opens Kinwall on a phone or computer without a key.

## Outcome

The device is a parent device for 30 days.

## Edge cases

- A passkey made at one address does not work at another; Kinwall says which address passkeys are set up for.
- Passkey sign-ins are limited to 20 every 10 minutes per address.
