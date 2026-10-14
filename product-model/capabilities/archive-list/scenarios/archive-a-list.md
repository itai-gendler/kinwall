---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Archive in a List's Edit sheet
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product moves it to Archived
  kind: product
  actor: parent
  entities:
  - {entity: list, effect: changes, from: Active, to: Archived, facts: []}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Archive a list

## Trigger

The camping trip is over.

## Outcome

The list leaves the Lists tab and waits under Archived.
