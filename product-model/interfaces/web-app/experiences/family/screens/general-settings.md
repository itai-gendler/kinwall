---
entities:
- entity: household
  shows:
  - Family name
  - Timezone
  - Week starts on
  - Default reminder
  - Chores & points
  - Lists
  - Features
  collects:
  - Family name
  - Timezone
  - Week starts on
  - Default reminder
  - Chores & points
  - Lists
  - Features
entryPoints:
- web-app: /#/settings?tab=general
references:
- kind: code
  role: implementation
  target: web/src/Settings.tsx#GeneralSection
---

# General settings

Settings → General: the household, the features that are on, and this device's own look.
