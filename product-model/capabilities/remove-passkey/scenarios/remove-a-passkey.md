---
kind: primary
routes:
  web: Web
steps:
- text: The Parent removes a Passkey under Parent devices and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: passkey, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product removes the Passkey and ends every sign-in made with it
  kind: product
  actor: parent
  entities:
  - {entity: passkey, effect: removes}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Remove a passkey

## Trigger

A phone is lost or replaced.

## Outcome

The passkey no longer signs anyone in, and its sessions are over.

## Edge cases

- Removing the last passkey warns first that an admin key or recovery code is then the only way in.
