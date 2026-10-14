---
kind: primary
routes:
  web: Web
steps:
- text: The Wall screen taps a ticked List item
  kind: actor
  actor: wall-screen
  entities:
  - {entity: list-item, effect: reads, facts: [Title, Checked off by]}
  contexts:
    web: {place: 'web-app::family::list'}
- text: The Product opens it again and clears who checked it off
  kind: product
  actor: wall-screen
  entities:
  - {entity: list-item, effect: changes, from: Checked off, to: Open, facts: [Checked off by, Steps]}
  contexts:
    web: {place: 'web-app::family::list'}
---

# Untick an item

## Trigger

An item was ticked by mistake.

## Outcome

The item is open again.
