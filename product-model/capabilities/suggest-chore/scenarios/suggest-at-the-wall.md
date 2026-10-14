---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen picks who is suggesting, then fills in and sends the idea
  kind: actor
  actor: wall-screen
  entities:
  - {entity: family-member, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product saves the Chore idea for that Family member
  kind: product
  actor: wall-screen
  entities:
  - {entity: chore-idea, effect: creates, to: Waiting for a grown-up, facts: [Title, Emoji, Points asked, Repeat, Day, Start time, Timer, Already did it]}
  - {entity: family-member, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Suggest a chore at the wall screen

## Trigger

A kid without a tablet suggests at the wall.

## Outcome

The idea waits for a grown-up.
