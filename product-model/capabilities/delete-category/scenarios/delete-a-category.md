---
kind: primary
routes:
  web: Web
steps:
- text: The Parent deletes a Category
  kind: actor
  actor: parent
  entities:
  - {entity: category, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product removes it and every event that used it falls back to its next category
  kind: product
  actor: parent
  entities:
  - {entity: category, effect: removes}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Delete a category

## Trigger

A category is no longer used.

## Outcome

No event shows the deleted category.
