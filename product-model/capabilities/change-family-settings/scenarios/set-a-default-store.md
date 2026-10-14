---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks a default grocery store and a default store for other shopping
  kind: actor
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: [Default stores]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves them, so Shop on a list of that type starts the trip there
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Default stores]}
  - {entity: list, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Set a default store

## Trigger

A family always shops at one market.

## Outcome

Shopping trips start at that store without asking.
