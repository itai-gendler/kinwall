---
availability:
- place: web-app::family
- place: web-app::welcome
references:
- kind: code
  role: implementation
  target: server/src/routes/settings.ts
- kind: code
  role: implementation
  target: web/src/Settings.tsx#GeneralSection
- kind: code
  role: implementation
  target: web/src/Settings.tsx#FeaturesSection
- kind: doc
  role: intent
  target: docs/settings/general.md
---

# Change general settings

Change the settings in Settings → General that every screen shares: the family name, timezone, week start and default reminder, and which features are on, here or in the setup wizard. A feature turned off disappears from every screen and phone; nothing is deleted.
