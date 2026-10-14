---
kind: primary
routes:
  web: Web
steps:
- text: The Parent adds a Category with a name, emoji, color and keywords
  kind: actor
  actor: parent
  entities:
  - {entity: category, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
- text: The Product saves it; events whose titles have a keyword now show in it
  kind: product
  actor: parent
  entities:
  - {entity: category, effect: creates, facts: [Name, Emoji, Color, Keywords]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::family-settings'}
---

# Add a category

## Trigger

A parent wants soccer games marked on the calendar.

## Outcome

Matching events take the category's emoji and color.
