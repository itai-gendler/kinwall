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
  target: web/src/outbox.ts
- kind: code
  role: implementation
  target: web/src/GetStuffDone.tsx
---

# Check off a list item

Tick an item off; it stays in place or moves to Done, as the list is set. Works offline and syncs when back online.
