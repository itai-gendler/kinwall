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
  target: web/src/trip.ts
---

# Clear checked items

Take the ticked items off a list, with Undo; at the end of a shopping trip, Done shopping also remembers the store they were bought at.
