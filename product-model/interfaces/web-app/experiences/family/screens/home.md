---
entities:
- entity: event
  shows:
  - Title
  - Starts
  - Ends
  - Who
  - Category
- entity: chore
  shows:
  - Title
  - Points
  - Assigned to
  - Start time
- entity: list-item
  shows:
  - Title
  - Due date
- entity: family-member
  shows:
  - Name
  - Avatar
  - Reward goal
  - Points to spend
- entity: household
  shows:
  - Family name
entryPoints:
- web-app: /#/home
references:
- kind: code
  role: implementation
  target: web/src/Board.tsx#Board
---

# Home

The Board: clock and weather, today, coming up, chores, lists due and reward goals, readable from across the room.
