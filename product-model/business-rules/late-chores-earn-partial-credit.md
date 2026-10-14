---
appliesTo:
- type: capability
  id: complete-chore
- type: capability
  id: approve-chore
- type: entity
  id: chore-completion
  facts:
  - Points earned
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#lateCompletionPoints
- kind: doc
  role: intent
  target: docs/using/chores.md
---

# A chore ticked for a past day earns the late completion credit

On its day or early it earns full points; for a past day it earns the household's Late completion credit share, rounded. A tick waiting for an OK is judged by when it was ticked, not when it was approved, and points are fixed then: changing a chore's points later doesn't change them.
