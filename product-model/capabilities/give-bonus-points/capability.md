---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/bonus-points.ts
- kind: code
  role: implementation
  target: web/src/GivePoints.tsx
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Give bonus points

Give a family member points for something that isn't a chore, with an optional note and the day they count on. They count like chore points but never change streaks. They exist while Chores & points is on.
