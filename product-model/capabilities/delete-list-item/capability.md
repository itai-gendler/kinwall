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
  target: web/src/Lists.tsx#SwipeRow
---

# Delete a list item

Delete an item, with a few seconds to undo.
