---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens a List, taps Edit and changes its name and owners
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name, Owners]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product saves it
  kind: product
  actor: parent
  entities:
  - {entity: list, effect: changes, facts: [Name, Owners]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Edit a list

## Trigger

A list becomes one kid's.

## Outcome

The list shows that kid as its owner.
