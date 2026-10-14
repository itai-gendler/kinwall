---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen opens Lists
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list, effect: reads, facts: [Name, Type, Open items]}
  contexts:
    web: {place: 'web-app::family::lists'}
- text: The Wall screen opens a List and reads its items
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list-item, effect: reads, facts: [Title, Quantity, Store, Aisle, Assign to, Due date, Added by, Checked off by]}
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Open a list

## Trigger

Someone checks the grocery list.

## Outcome

The list's items show, grouped and sorted the way it is set to.

## Edge cases

- A list with overdue to-dos says so on its card.
