---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen opens Home
  kind: actor
  actor: wall-screen
  entities: []
  contexts:
    web: {place: 'web-app::family::home'}
- text: The Wall screen reads today's events, what's coming up, chores left, things due and who is saving for what
  kind: actor
  actor: wall-screen
  entities:
  - {entity: event, effect: reads, facts: [Title, Starts, Ends, Who, Category]}
  - {entity: chore, effect: reads, facts: [Title, Points, Assigned to, Start time]}
  - {entity: list-item, effect: reads, facts: [Title, Due date]}
  - {entity: family-member, effect: reads, facts: [Name, Avatar, Reward goal, Points to spend]}
  contexts:
    web: {place: 'web-app::family::home'}
---

# Look at the Board

## Trigger

The family glances at the wall in the morning.

## Outcome

Everyone sees the day at a glance.

## Edge cases

- Each screen can have its own layout, such as big and simple for the kids or meals first in the kitchen.
- A free event shows faded and is never Now or Next.
