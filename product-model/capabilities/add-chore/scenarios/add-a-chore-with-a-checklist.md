---
kind: primary
routes:
  web: Web
steps:
- text: The Parent adds a daily Bedtime chore and picks the Bedtime List as its checklist
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name, Type]}
  - {entity: chore, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product adds the Chore; its card shows the checklist's progress
  kind: product
  actor: parent
  entities:
  - {entity: chore, effect: creates, to: Active, facts: [Title, Emoji, Points, Assigned to, Repeat, Due date, Start time, Timer, Checklist, Needs a parent's
        OK]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Add a chore with a checklist

## Trigger

A routine has several steps.

## Outcome

The chore can only be completed once its checklist is ticked off.
