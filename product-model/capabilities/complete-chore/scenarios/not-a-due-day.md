---
kind: validation
routes:
  web: Web
steps:
- text: The Wall screen ticks a Chore for a day it is not due, or more than a week back
  kind: actor
  actor: wall-screen
  entities:
  - {entity: chore, effect: reads, facts: [Title, Repeat]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The day is not one the chore is due on, or is outside the days a wall screen may tick
  kind: condition
  entities:
  - {entity: wall-screen, effect: reads, facts: []}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product says the chore isn't due that day, or that older days are for a parent's device
  kind: product
  actor: wall-screen
  entities:
  - {entity: parent, effect: reads, facts: []}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# A chore cannot be ticked for a day it is not due

## Trigger

Someone ticks a chore for the wrong day.

## Outcome

Nothing is ticked.
