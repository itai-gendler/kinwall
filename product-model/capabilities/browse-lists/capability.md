---
availability:
- place: web-app::family
domain: lists
references:
- kind: code
  role: implementation
  target: web/src/Lists.tsx
- kind: code
  role: implementation
  target: server/src/routes/lists.ts
- kind: doc
  role: intent
  target: docs/using/lists.md
---

# Browse lists

See the family's lists grouped by type with how many items are open, and open one to see its items. It exists while Lists is on.
