---
entities:
- entity: chore
  shows:
  - Title
  - Emoji
  - Points
  - Assigned to
  - Repeat
  - Due date
  - Start time
  - Timer
  - Checklist
  - Needs a parent's OK
  collects:
  - Title
  - Emoji
  - Points
  - Assigned to
  - Repeat
  - Due date
  - Start time
  - Timer
  - Checklist
  - Needs a parent's OK
- entity: chore-completion
  shows:
  - Day
  - Done by
  - Points earned
  - Ticked at
  - Not yet note
  collects:
  - Not yet note
- entity: chore-idea
  shows:
  - Title
  - Emoji
  - Points asked
  - Repeat
  - Already did it
  - Note
  collects:
  - Title
  - Emoji
  - Points asked
  - Repeat
  - Day
  - Start time
  - Timer
  - Already did it
  - Note
- entity: family-member
  shows:
  - Name
  - Color
  - Avatar
  - Points earned
  - Points to spend
  - Streak
- entity: bonus-points
  shows:
  - Points
  - Note
  - Day
  collects:
  - Points
  - Note
  - Day
- entity: reward-request
  shows:
  - Points
  - Shares
- entity: list
  shows:
  - Name
  - Type
entryPoints:
- web-app: /#/chores
references:
- kind: code
  role: implementation
  target: web/src/Chores.tsx#Chores
---

# Chores

A day's chores by person, the leaderboard, chores and reward requests waiting for a parent, chore ideas and bonus points.
