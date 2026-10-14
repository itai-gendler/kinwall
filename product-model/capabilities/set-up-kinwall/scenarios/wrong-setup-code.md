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
- text: The code is not the one in the server log
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::welcome::setup'}
- text: The Product says "That code didn't work" and leaves Kinwall unclaimed
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::setup'}
---

# A wrong setup code is refused

## Trigger

A parent mistypes the setup code.

## Outcome

Nothing is claimed; the parent can try again.
