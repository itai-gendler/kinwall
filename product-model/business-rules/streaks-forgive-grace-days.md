---
appliesTo:
- type: capability
  id: view-leaderboard
- type: entity
  id: family-member
  facts:
  - Streak
references:
- kind: code
  role: implementation
  target: server/src/routes/leaderboard.ts
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# A streak counts days on which every chore due was done, forgiving the streak grace

Days with nothing due are skipped; today counts once its chores are done; a streak survives the household's Streak grace missed days in any rolling week, looking back at most 60 days.
