---
appliesTo:
- type: capability
  id: add-chore
- type: capability
  id: edit-chore
references:
- kind: code
  role: implementation
  target: server/src/recurrence.ts#isValidRrule
- kind: code
  role: implementation
  target: server/src/routes/chores.ts#choreRepeatError
---

# A chore repeats daily or slower, on days that happen

A repeat within a day, such as hourly, is refused, and so is one that never happens, like the 30th of February.
