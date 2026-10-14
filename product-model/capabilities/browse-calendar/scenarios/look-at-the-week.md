---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen opens Calendar and picks Week
  kind: actor
  actor: wall-screen
  entities:
  - {entity: calendar, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
- text: The Wall screen reads each Event in its person's color, with its category and leave-by time
  kind: actor
  actor: wall-screen
  entities:
  - {entity: event, effect: reads, facts: [Title, Starts, Ends, All day, Who, Category, Show as, Travel time]}
  - {entity: category, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::calendar'}
---

# Look at the week

## Trigger

The family plans the week.

## Outcome

Everyone sees the week's events across all calendars.

## Edge cases

- Tapping a person or a category narrows the calendar to them.
- An event that shows on two calendars shows once.
