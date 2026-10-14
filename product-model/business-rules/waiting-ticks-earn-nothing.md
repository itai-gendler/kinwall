---
appliesTo:
- type: entity
  id: chore-completion
  effect: creates
  to: Waiting for OK
- type: capability
  id: approve-chore
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts
---

# A tick waiting for a parent's OK earns nothing yet

It doesn't count toward points, streaks, the leaderboard, balances or done counts until it is approved.
