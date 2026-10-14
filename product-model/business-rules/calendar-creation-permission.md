---
appliesTo:
- type: entity
  id: calendar
  effect: creates
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/calendars.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents add calendars

Calendar setup is for parent devices.
