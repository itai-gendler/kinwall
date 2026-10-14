---
kind: primary
routes:
  web: Web
steps:
- text: The Parent approves a Chore idea marked I already did it today
  kind: actor
  actor: parent
  entities:
  - {entity: chore-idea, effect: reads, facts: [Title, Already did it]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product makes the Chore and marks it done today, so the kid gets the points now, once
  kind: product
  actor: parent
  entities:
  - {entity: chore-idea, effect: changes, from: Waiting for a grown-up, to: Approved, facts: [Note, Answered by]}
  - {entity: chore, effect: creates, to: Active, facts: [Title, Emoji, Points, Assigned to, Repeat, Due date, Start time, Timer, Checklist, Needs a parent's
        OK]}
  - {entity: chore-completion, effect: creates, to: Done, facts: [Day, Done by, Points earned, Ticked at], with: chore}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Say yes to something already done

## Trigger

A kid already cleaned up the garage.

## Outcome

The chore is done today with its points.
