---
entities:
- entity: family-member
  shows:
  - Name
  - Color
  - Avatar
  - Birthday
  - Grown-up
  - Their chores need a parent's OK
  collects:
  - Name
  - Color
  - Avatar
  - Birthday
  - Grown-up
  - Their chores need a parent's OK
- entity: category
  shows:
  - Name
  - Emoji
  - Color
  - Keywords
  collects:
  - Name
  - Emoji
  - Color
  - Keywords
- entity: household
  shows:
  - Late completion credit
  - Streak grace
  - Leaderboard
  - Rewards
  - Kids can suggest chores
  - Default stores
  collects:
  - Late completion credit
  - Streak grace
  - Leaderboard
  - Rewards
  - Kids can suggest chores
  - Default stores
entryPoints:
- web-app: /#/settings?tab=family
references:
- kind: code
  role: implementation
  target: web/src/Settings.tsx#MembersSection
- kind: code
  role: implementation
  target: web/src/Settings.tsx#CategoriesSection
---

# Family settings

Settings → Family: the members, the event categories, and the chore and shopping settings.
