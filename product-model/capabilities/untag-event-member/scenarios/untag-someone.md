---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps a tagged Family member's chip on an Event
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title, Who]}
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product takes the tag off at once
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, facts: [Who]}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Untag someone from an event

## Trigger

Someone is not going after all.

## Outcome

The event leaves that person's day.

## Edge cases

- Untagging everyone leaves the event to the calendar's members again.
