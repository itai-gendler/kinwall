---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps a Family member's chip on an Event
  kind: actor
  actor: wall-screen
  entities:
  - {entity: event, effect: reads, facts: [Title, Who]}
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product tags them at once
  kind: product
  actor: wall-screen
  entities:
  - {entity: event, effect: changes, facts: [Who]}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Tag someone on an event

## Trigger

Dad is driving to practice.

## Outcome

The event shows on Dad's day too.
