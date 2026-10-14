---
kind: validation
routes:
  web: Web
steps:
- text: The Parent enters a recovery code
  kind: actor
  actor: parent
  entities:
  - {entity: recovery-code, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
- text: The code is unknown or was already used
  kind: condition
  entities: []
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
- text: The Product says the recovery code is not valid
  kind: product
  actor: parent
  entities:
  - {entity: recovery-code, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::welcome::sign-in'}
---

# A used or unknown recovery code is refused

## Trigger

A parent enters a code that does not work.

## Outcome

Nobody is signed in.

## Edge cases

- After 10 tries in an hour from one address (30 overall) Kinwall asks to try again later.
