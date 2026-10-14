---
kind: primary
routes:
  web: Web
steps:
- text: The Parent removes a Paired device under Paired devices
  kind: actor
  actor: parent
  entities:
  - {entity: paired-device, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::administration::access'}
- text: The Product removes it and signs it out, with the widgets and Watch that went with it
  kind: product
  actor: parent
  entities:
  - {entity: paired-device, effect: removes, from: Paired}
  contexts:
    web: {place: 'web-app::administration::access'}
---

# Remove a paired device

## Trigger

A tablet is replaced or given away.

## Outcome

The device needs a new code and a parent to use Kinwall again.
