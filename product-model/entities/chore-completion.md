---
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#completeChore
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Chore completion

A chore ticked off for one day, crediting whoever did it.

## Information kept

- **Day** — the day it was done for
- **Done by** — who earns the points, or nobody in particular
- **Points earned** — what it earned, fixed when it was ticked
- **Ticked at** — when it was ticked
- **Not yet note** — a parent's note when they sent it back

## States

### Done

Counted: it earns its points and counts toward streaks and the leaderboard.

### Waiting for OK

Ticked on a wall screen or a kid's device and waiting for a parent; it earns nothing yet.

### Not yet

A parent sent it back, with an optional note the kid sees until they tick it again.
