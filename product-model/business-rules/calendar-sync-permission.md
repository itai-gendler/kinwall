---
appliesTo:
- type: entity
  id: calendar
  effect: changes
  facts:
  - Last synced
  - Sync status
permits:
- actors:
  - parent
- unattended: true
references:
- kind: code
  role: implementation
  target: server/src/sync.ts#syncDue
---

# Calendars are synced by parents or on Kinwall's own schedule

Sync now is on parents' devices; every calendar also syncs on its own.
