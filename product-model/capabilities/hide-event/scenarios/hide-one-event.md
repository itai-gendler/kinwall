---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens an Event and picks Hide… for this event
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product hides it everywhere the family sees events
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, from: Shown, to: Hidden, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Hide an event

## Trigger

A school feed lists a meeting nobody goes to.

## Outcome

The event is gone from every screen.
