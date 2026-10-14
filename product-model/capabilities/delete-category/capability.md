---
availability:
- place: web-app::family
domain: family
references:
- kind: code
  role: implementation
  target: server/src/routes/categories.ts
- kind: doc
  role: intent
  target: docs/using/categories.md
---

# Delete a category

Delete an event category; events that used it fall back to their series, a keyword match or their calendar's default.
