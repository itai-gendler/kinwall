---
kind: primary
routes:
  web: Web
steps:
- text: The Parent turns on Default Groceries list for a List
  kind: actor
  actor: parent
  entities:
  - {entity: list, as: new-default, effect: reads, facts: [Type, Default]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product makes it the default and turns it off on the other Groceries list
  kind: product
  actor: parent
  entities:
  - {entity: list, as: new-default, effect: changes, facts: [Default]}
  - {entity: list, as: previous-default, effect: changes, facts: [Default]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Make a list the default of its type

## Trigger

A family has two grocery lists.

## Outcome

Barcode scans, meal ingredients and the app's shortcuts use the default list.
