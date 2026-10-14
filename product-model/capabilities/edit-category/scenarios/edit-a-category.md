---
kind: primary
routes:
  web: Web
steps:
- text: The Parent changes a Category's name, emoji, color or keywords
  kind: actor
  actor: parent
  entities:
  - {entity: category, effect: reads, facts: [Name, Emoji, Color, Keywords]}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves it; events are sorted again by the new keywords
  kind: product
  actor: parent
  entities:
  - {entity: category, effect: changes, facts: [Name, Emoji, Color, Keywords]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Edit a category

## Trigger

A category catches the wrong events.

## Outcome

Events show under the category their titles now match.
