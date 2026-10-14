---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chore-suggestions.ts
- kind: code
  role: implementation
  target: web/src/ChoreSuggest.tsx
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Suggest a chore

Send a chore idea with the points a kid thinks it is worth, for a grown-up to say yes to. It exists while Chores & points and Kids can suggest chores are on.
