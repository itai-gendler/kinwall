---
appliesTo:
- type: entity
  id: list
  effect: changes
  facts:
  - Last done
permits:
- actors:
  - parent
- actors:
  - wall-screen
- actors:
  - kid
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts#resetListItems
---

# A reusable list is reset from any device

A parent's device, a wall screen or a kid's device records who finished a reusable list when it resets it.
