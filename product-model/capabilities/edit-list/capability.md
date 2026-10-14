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
  target: web/src/Lists.tsx#ListEditSheet
---

# Edit a list

Change a list's name, type, emoji, color, owners, whether checked items stay in place, and whether it is the default for its type.
