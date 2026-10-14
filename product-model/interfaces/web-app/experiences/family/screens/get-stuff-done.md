---
entities:
- entity: list
  shows:
  - Name
- entity: list-item
  shows:
  - Title
  - Steps
- entity: chore
  shows:
  - Title
references:
- kind: code
  role: implementation
  target: web/src/GetStuffDone.tsx#GetStuffDone
---

# Get stuff done

A list full screen, one item at a time or the whole list, as a chore's checklist or a routine on the Board.
