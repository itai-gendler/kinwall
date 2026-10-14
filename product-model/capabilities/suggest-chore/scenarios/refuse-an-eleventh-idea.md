---
kind: validation
routes:
  web: Web
steps:
- text: The Kid sends another idea
  kind: actor
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Kid already has 10 ideas waiting
  kind: condition
  actor: kid
  entities:
  - {entity: chore-idea, effect: reads, facts: []}
  contexts:
    web: {place: 'web-app::family::chores'}
- text: The Product says they already have 10 ideas waiting for a grown-up
  kind: product
  actor: kid
  entities: []
  contexts:
    web: {place: 'web-app::family::chores'}
---

# Ten ideas already waiting

## Trigger

A kid sends idea after idea.

## Outcome

Nothing more is sent until a grown-up answers some.
