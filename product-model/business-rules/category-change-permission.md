---
appliesTo:
- type: entity
  id: category
  effect: changes
permits:
- actors:
  - parent
references:
- kind: code
  role: implementation
  target: server/src/routes/categories.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#isDisplayAllowed
---

# Only parents change categories

Wall screens and kids' devices read categories; parents change them.
