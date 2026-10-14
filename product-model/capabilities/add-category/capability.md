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
- kind: doc
  role: intent
  target: docs/using/categories.md
---

# Add a category

Add an event category with a name, emoji, color and the keywords that sort events into it.
