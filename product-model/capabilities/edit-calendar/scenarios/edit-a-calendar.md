---
kind: primary
routes:
  web: Web
steps:
- text: The Parent opens Edit calendar and changes its name, color, members, default category or filter
  kind: actor
  actor: parent
  entities:
  - {entity: calendar, effect: reads, facts: [Name, Color, Members, Default category, Filter]}
  - {entity: category, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
- text: The Product saves it; the family sees its events with the new settings without a resync
  kind: product
  actor: parent
  entities:
  - {entity: calendar, effect: changes, facts: [Name, Color, Members, Default category, Filter]}
  - {entity: event, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::administration::calendar-details'}
---

# Edit a calendar

## Trigger

A school calendar is too busy.

## Outcome

Only the matching events show, in the calendar's new color and category.
