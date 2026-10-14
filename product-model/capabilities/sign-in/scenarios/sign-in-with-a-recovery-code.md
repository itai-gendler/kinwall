---
kind: primary
routes:
  web: Web
steps:
- text: The Parent chooses Use a recovery code and enters one
  kind: actor
  actor: parent
  entities:
  - {entity: recovery-code, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
- text: The Product spends the Recovery code and starts a 30-day parent session that belongs to no one
  kind: product
  actor: parent
  entities:
  - {entity: recovery-code, effect: changes, from: Unused, to: Used, facts: []}
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
---

# Sign in with a recovery code

## Trigger

Every passkey device is lost.

## Outcome

The parent is signed in and can add a new passkey; that code never works again.
