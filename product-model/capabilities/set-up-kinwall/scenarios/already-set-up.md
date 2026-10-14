---
kind: validation
routes:
  web: Web
steps:
- text: The Parent enters a setup code
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The family already set this Kinwall up
  kind: condition
  entities:
  - {entity: household, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product says this Kinwall is already set up
  kind: product
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# A Kinwall already set up cannot be claimed again

## Trigger

Someone opens the setup link of a family that is already set up.

## Outcome

Nothing changes; the family keeps its Kinwall.
