---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Create a passkey for this device in the setup wizard and confirms
  kind: actor
  actor: parent
  entities:
  - {entity: passkey, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product saves the Passkey and moves on to the recovery codes
  kind: product
  actor: parent
  entities:
  - {entity: passkey, effect: creates, facts: [Name, Whose device, Added]}
  - {entity: recovery-code, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# Create a passkey in the setup wizard

## Trigger

A parent has just claimed Kinwall.

## Outcome

The device signs in with a passkey from now on.

## Edge cases

- There is no Skip: when the browser can't make a passkey, the wizard moves on to recovery codes as the way back in.
