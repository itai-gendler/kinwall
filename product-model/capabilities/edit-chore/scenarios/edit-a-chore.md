---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Edit chores, then a Chore, and changes its points and days
  kind: actor
  actor: parent
  entities:
  - {entity: chore, effect: reads, facts: [Title, Emoji, Points, Assigned to, Repeat, Due date, Start time, Timer, Checklist, Needs a parent's OK]}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product saves it; ticks already made keep the points they earned
  kind: product
  actor: parent
  entities:
  - {entity: chore, effect: changes, facts: [Points, Repeat]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Edit a chore

## Trigger

A chore is worth more now.

## Outcome

Future ticks earn the new points.

## Edge cases

- A rule set through the API, such as every other week, shows as a custom schedule and is kept unless another repeat is picked.
