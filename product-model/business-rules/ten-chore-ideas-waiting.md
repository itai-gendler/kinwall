---
appliesTo:
- type: capability
  id: suggest-chore
- type: entity
  id: chore-idea
  effect: creates
  to: Waiting for a grown-up
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
---

# A kid has at most 10 chore ideas waiting at once

Answering some lets them send more.
