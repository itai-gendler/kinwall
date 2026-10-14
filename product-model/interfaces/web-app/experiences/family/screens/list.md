---
entities:
- entity: list
  shows:
  - Name
  - Type
  - Owners
  - Default
  - Keep checked items in place
  - Last done
  collects:
  - Name
  - Type
  - Emoji
  - Color
  - Owners
  - Keep checked items in place
  - Default
- entity: list-item
  shows:
  - Title
  - Quantity
  - Store
  - Aisle
  - Department
  - On sale
  - For
  - Assign to
  - Due date
  - Priority
  - Steps
  - Linked event
  - Notes
  - Added by
  - Checked off by
  collects:
  - Title
  - Quantity
  - Store
  - Aisle
  - Department
  - On sale
  - For
  - Assign to
  - Due date
  - Priority
  - Steps
  - Linked event
  - Notes
references:
- kind: code
  role: implementation
  target: web/src/Lists.tsx#ItemEditSheet
---

# List

One open list with its items, where they are added, ticked, edited, moved and cleared.
