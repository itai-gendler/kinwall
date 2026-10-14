---
kind: primary
routes:
  web: Web
steps:
- text: The Product makes eight codes and shows them with Copy all and Download .txt
  kind: product
  actor: parent
  entities:
  - {entity: recovery-code, effect: creates, to: Unused, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Parent saves the codes and continues
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# Save recovery codes in the setup wizard

## Trigger

The wizard reaches the recovery codes step.

## Outcome

The family has its way back in if every passkey device is lost.

## Edge cases

- Without a passkey the codes are the only way back in, so the step has no Skip for now.
