---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps New list, names it and picks a type
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::lists'}
- text: The Product adds the List at the end of its type's section
  kind: product
  actor: wall-screen
  entities:
  - {entity: list, effect: creates, to: Active, facts: [Name, Type, Emoji, Color, Owners, Keep checked items in place, Default]}
  contexts:
    web: {place: 'web-app::family::lists'}
---

# Create a list

## Trigger

The family plans a camping trip.

## Outcome

Everyone sees the new list.

## Edge cases

- Shopping and reusable lists keep checked items in place to start; to-do lists move them to Done.
