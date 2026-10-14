---
availability:
- place: web-app::family
domain: chores
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#completeChore
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#lateCompletionPoints
- kind: code
  role: implementation
  target: web/src/Chores.tsx#ChoreCard
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# Complete a chore

Tick a chore off for a day it is due. Whoever did it earns its points: full points on its day or early, the late completion credit for a past day. A tick from a wall screen or a kid's device waits for a parent's OK when the chore or the person needs one. They exist while Chores & points is on.
