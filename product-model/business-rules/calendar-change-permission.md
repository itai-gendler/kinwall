---
appliesTo:
- type: entity
  id: calendar
  effect: changes
  facts:
  - Name
  - Color
  - Members
  - Default category
  - Filter
  - Enabled
  - Wall screens and kids' devices can edit
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

# Only parents change a calendar's settings

Calendar setup is for parent devices.
