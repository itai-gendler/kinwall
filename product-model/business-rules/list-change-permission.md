---
appliesTo:
- type: entity
  id: list
  effect: changes
  facts:
  - Name
  - Type
  - Emoji
  - Color
  - Owners
  - Default
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents change a list itself

A list's name, type, emoji, color, owners and default are changed from parent devices; a wall screen or kid's device only changes how it is sorted, grouped and shown.
