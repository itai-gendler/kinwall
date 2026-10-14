---
kind: primary
routes:
  web: Web
steps:
- text: The Parent taps Change under Features and turns one of them off
  kind: actor
  actor: parent
  entities:
  - {entity: household, effect: reads, facts: [Chores & points, Lists, Features]}
  contexts:
    web: {place: 'web-app::family::general-settings'}
- text: The Product hides that feature on every screen and phone and keeps everything in it
  kind: product
  actor: parent
  entities:
  - {entity: household, effect: changes, facts: [Chores & points, Lists, Features]}
  contexts:
    web: {place: 'web-app::family::general-settings'}
---

# Turn a feature off

## Trigger

A family does not use chores.

## Outcome

The feature is gone from every screen; turning it back on brings everything back as it was.
