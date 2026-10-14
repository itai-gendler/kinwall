---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Say yes… on a Chore idea, changes the points, adds "Great idea!" and taps Approve
  kind: actor
  actor: parent
  entities:
  - {entity: chore-idea, effect: reads, facts: [Title, Points asked, Repeat, Already did it]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product makes it a Chore for the kid and tells the kid's devices
  kind: product
  actor: parent
  entities:
  - {entity: chore-idea, effect: changes, from: Waiting for a grown-up, to: Approved, facts: [Note, Answered by]}
  - {entity: chore, effect: creates, to: Active, facts: [Title, Emoji, Points, Assigned to, Repeat, Due date, Start time, Timer, Checklist, Needs a parent's
        OK]}
  - {entity: kid, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Say yes to a chore idea

## Trigger

A parent likes the idea.

## Outcome

The kid sees "Sam said yes! Piano practice · 4 points".
