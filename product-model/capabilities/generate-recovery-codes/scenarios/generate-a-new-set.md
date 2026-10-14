---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Generate recovery codes
  kind: actor
  actor: parent
  entities:
  - {entity: recovery-code, as: old-code, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product makes eight new codes, shows them once with Copy all and Download, and retires the old set
  kind: product
  actor: parent
  entities:
  - {entity: recovery-code, as: new-code, effect: creates, to: Unused, facts: []}
  - {entity: recovery-code, as: old-code, effect: removes, from: Unused}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Generate a new set of recovery codes

## Trigger

A parent wants a way back in if every passkey device is lost.

## Outcome

The family has eight fresh codes; the old ones stopped working at once.

## Edge cases

- The section shows how many of the eight are left, never the codes again.
