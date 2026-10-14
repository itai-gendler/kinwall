---
entities:
- entity: list
  shows:
  - Name
  - Type
  - Emoji
  - Color
  - Owners
  - Default
  - Open items
  collects:
  - Name
  - Type
  - Emoji
  - Color
  - Owners
  - Keep checked items in place
  - Default
entryPoints:
- web-app: /#/lists
references:
- kind: code
  role: implementation
  target: web/src/Lists.tsx
---

# Lists

The family's lists grouped by type, with their open items, and the Archived section on a parent's device.
