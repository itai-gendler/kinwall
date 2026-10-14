---
availability:
- place: web-app::family
domain: family
references:
- kind: code
  role: implementation
  target: server/src/routes/settings.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#ChoreSettingsSection
- kind: code
  role: implementation
  target: web/src/Settings.tsx#ShoppingSettingsSection
- kind: doc
  role: intent
  target: docs/settings/family.md
---

# Change family settings

Change the family's chore and shopping settings in Settings → Family: late completion credit, streak grace, the leaderboard, rewards, kids suggesting chores and each shopping list type's default store.
