---
kind: primary
routes:
  web: Web
steps:
- text: The Parent sets a travel time on an Event from an ICS feed
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title, Travel time]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product keeps the travel time in Kinwall only and shows a leave-by time
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, facts: [Travel time]}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Set travel time on a read-only event

## Trigger

The family needs to leave early for a school concert.

## Outcome

The event shows when to leave.
