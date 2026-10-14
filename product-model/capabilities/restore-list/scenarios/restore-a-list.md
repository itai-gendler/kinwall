---
kind: primary
routes:
  web: Web
steps:
- text: The Parent expands Archived and taps Restore on a List
  kind: actor
  actor: parent
  entities:
  - {entity: list, effect: reads, facts: [Name]}
  contexts:
    web: {place: 'web-app::family::lists'}
- text: The Product brings it back where it was
  kind: product
  actor: parent
  entities:
  - {entity: list, effect: changes, from: Archived, to: Active, facts: []}
  contexts:
    web: {place: 'web-app::family::lists'}
---

# Restore a list

## Trigger

Camping season is back.

## Outcome

The list is on the Lists tab again.
