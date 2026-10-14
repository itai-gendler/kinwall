---
kind: primary
routes:
  web: Web
steps:
- text: The Parent picks Hide… for every event in the series
  kind: actor
  actor: parent
  entities:
  - {entity: event, effect: reads, facts: [Title, Repeat]}
  contexts:
    web: {place: 'web-app::family::event'}
- text: The Product hides every event in the series, now and after each sync
  kind: product
  actor: parent
  entities:
  - {entity: event, effect: changes, from: Shown, to: Hidden, facts: []}
  contexts:
    web: {place: 'web-app::family::event'}
---

# Hide a whole series

## Trigger

A weekly club no one in the family attends.

## Outcome

None of its events show.
