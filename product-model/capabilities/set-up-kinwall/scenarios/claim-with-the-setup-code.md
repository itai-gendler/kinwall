---
kind: primary
routes:
  web: Web
steps:
- text: The Parent enters the 6-digit setup code and continues
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product claims Kinwall for the family and signs this device in as a parent device
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, from: Unclaimed, to: Set up, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The setup wizard moves on to creating a passkey for this device
  kind: condition
  entities:
  - {entity: household, effect: reads, facts: []}
  - {entity: passkey, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# Claim Kinwall with the setup code

## Trigger

A parent opens a Kinwall nobody has set up yet.

## Outcome

Kinwall belongs to the family, this device is a parent device, and the wizard carries on with the passkey step.

## Edge cases

- The server's admin key works in place of the setup code.
- Claim attempts are limited to 10 an hour.
