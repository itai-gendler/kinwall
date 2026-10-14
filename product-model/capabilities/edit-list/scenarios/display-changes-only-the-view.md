---
kind: validation
routes:
  web: Web
steps:
- text: The Wall screen tries to rename a List
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The device is a wall screen
  kind: condition
  entities:
  - {entity: wall-screen, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product says "Ask a grown-up to change this list."
  kind: product
  actor: wall-screen
  entities:
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::list'}
---

# A wall screen changes only how a list is shown

## Trigger

Someone at the wall renames the grocery list.

## Outcome

The list keeps its name; sorting and grouping can still change.
