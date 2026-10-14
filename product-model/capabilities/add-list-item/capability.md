---
availability:
- place: web-app::family
domain: lists
references:
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: code
  role: implementation
  target: server/src/item-memory.ts
- kind: doc
  role: intent
  target: docs/using/lists.md
---

# Add a list item

Add one or more items to a list from any device. On a Groceries or Shopping list, a name the family added before brings back its store, aisle and department.
