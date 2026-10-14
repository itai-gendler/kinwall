---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Not this time on a Chore idea and adds a reason
  kind: actor
  actor: parent
  entities:
  - {entity: chore-idea, effect: reads, facts: [Title]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product saves the answer and tells the kid's own devices
  kind: product
  actor: parent
  entities:
  - {entity: chore-idea, effect: changes, from: Waiting for a grown-up, to: Not this time, facts: [Note, Answered by]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Say Not this time to a chore idea

## Trigger

The idea does not fit.

## Outcome

The kid sees "Not this time" with the reason on their own device, never on a shared wall screen.
