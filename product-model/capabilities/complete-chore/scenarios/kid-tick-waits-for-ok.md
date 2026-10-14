---
kind: primary
routes:
  web: Web
steps:
- text: The Kid taps their Chore on their own device
  kind: actor
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: [Title, Points]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Chore needs a parent's OK, by its own setting or the Kid's
  kind: condition
  actor: kid
  entities:
  - {entity: chore, effect: reads, facts: [Needs a parent's OK]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product marks it Waiting for OK and tells parents' devices "Leo finished Make bed. Approve?"
  kind: product
  actor: kid
  entities:
  - {entity: chore-completion, effect: creates, to: Waiting for OK, facts: [Day, Done by, Points earned, Ticked at]}
  - {entity: parent, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A kid's tick waits for a parent's OK

## Trigger

A kid makes their bed.

## Outcome

The card shows an hourglass; no points count until a parent approves.
