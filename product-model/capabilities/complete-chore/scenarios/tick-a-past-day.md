---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks yesterday on the date strip and taps a Chore
  kind: actor
  actor: parent
  entities:
  - {entity: chore, effect: reads, facts: [Title, Points]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product marks it done for that day with the late completion credit, rounded
  kind: product
  actor: parent
  entities:
  - {entity: chore-completion, effect: creates, to: Done, facts: [Day, Done by, Points earned, Ticked at]}
  - {entity: household, effect: reads, facts: [Late completion credit]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Tick a chore for a past day

## Trigger

A chore was done but not ticked yesterday.

## Outcome

It counts for yesterday with partial points.
