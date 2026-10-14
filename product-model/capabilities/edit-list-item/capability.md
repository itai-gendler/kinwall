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
  target: web/src/Lists.tsx#ItemEditSheet
---

# Edit a list item

Change an item's title, quantity, store, aisle, department, sale tag, who it is for or assigned to, due date, priority or notes.
