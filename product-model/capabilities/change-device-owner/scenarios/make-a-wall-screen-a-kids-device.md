---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks a kid for a Paired device under Paired devices
  kind: actor
  actor: parent
  entities:
  - {entity: paired-device, effect: reads, facts: [Name, What it is, Whose device]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product makes it that kid's device and leaves a privacy note on the kid's own devices
  kind: product
  actor: parent
  entities:
  - {entity: paired-device, effect: changes, facts: [What it is, Whose device]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Make a wall screen a kid's device

## Trigger

A family tablet becomes one kid's.

## Outcome

The device now shows only that kid's things.
