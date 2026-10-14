---
appliesTo:
- type: entity
  id: calendar
  effect: removes
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

# Only parents remove calendars

Calendar setup is for parent devices.
