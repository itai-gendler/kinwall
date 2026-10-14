---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen opens Chores
  kind: actor
  actor: wall-screen
  entities:
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Wall screen reads each person's chores for today, their points and what is done or waiting for OK
  kind: actor
  actor: wall-screen
  entities:
  - {entity: chore, effect: reads, facts: [Title, Emoji, Points, Assigned to, Start time, Checklist]}
  - {entity: chore-completion, effect: reads, facts: [Done by, Not yet note]}
  - {entity: family-member, effect: reads, facts: [Name, Points earned, Points to spend, Streak]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Look at today's chores

## Trigger

The kids check what is left to do.

## Outcome

Everyone sees their chores and progress for the day.
