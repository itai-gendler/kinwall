---
appliesTo:
- type: capability
  id: complete-chore
  contexts:
  - place: web-app::family
- type: entity
  id: chore-completion
  facts:
  - Day
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#completeChore
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#dueOnDate
---

# A chore is ticked only for a day it is due, and from a wall screen or kid's device only from a week back to a day ahead

Older days are fixed up from a parent's device. A one-off chore with no day set is ticked once, for any day.
