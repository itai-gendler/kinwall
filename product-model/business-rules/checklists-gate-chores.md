---
appliesTo:
- type: capability
  id: complete-chore
- type: capability
  id: reset-list
references:
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#completeChore
---

# A chore with a checklist completes only once that person's checklist items are all ticked

The checklist counts the list's items for the chore's person (or whoever does an Anyone chore) plus unassigned ones. Completing the chore resets a reusable checklist for that person and the shared items.
