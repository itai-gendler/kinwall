---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/leaderboard.ts
- kind: code
  role: implementation
  target: web/src/Chores.tsx#Leaderboard
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# View the leaderboard

See family members ranked by the points they earned today, this week or this month, with their streaks and points to spend. It shows while the family's Leaderboard setting is on.
