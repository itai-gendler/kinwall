---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps an Anyone Chore and picks who did it under Who did it?
  kind: actor
  actor: wall-screen
  entities:
  - {entity: chore, effect: reads, facts: [Title, Assigned to]}
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product marks it done and credits that Family member
  kind: product
  actor: wall-screen
  entities:
  - {entity: chore-completion, effect: creates, to: Done, facts: [Day, Done by, Points earned, Ticked at]}
  - {entity: family-member, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Someone at the wall ticks an Anyone chore

## Trigger

Whoever fed the dog ticks it on the wall.

## Outcome

The card says "Done by Sam".

## Edge cases

- Nobody in particular credits no one.
- With the family filtered to one person, or on a kid's device, it counts for that person without asking.
