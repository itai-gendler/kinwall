---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps +, enters a title, emoji and points, picks who and Weekly on Mon, Wed and Fri
  kind: actor
  actor: parent
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product adds the Chore, due from today on the picked days
  kind: product
  actor: parent
  entities:
  - {entity: chore, effect: creates, to: Active, facts: [Title, Emoji, Points, Assigned to, Repeat, Due date, Start time, Timer, Checklist, Needs a parent's
        OK]}
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Add a weekly chore

## Trigger

A parent sets up who takes out the trash.

## Outcome

The chore shows on that person's column on its days.
