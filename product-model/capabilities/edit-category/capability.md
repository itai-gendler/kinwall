---
availability:
- place: web-app::family
domain: family
references:
- kind: code
  role: implementation
  target: server/src/routes/categories.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#CategoryEditSheet
---

# Edit a category

Change a category's name, emoji, color or keywords.
