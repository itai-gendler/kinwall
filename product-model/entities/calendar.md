---
domain: calendars
relations:
- entity: event
  verb: holds
  cardinality: one-to-many
- entity: family-member
  verb: serves
  cardinality: many-to-many
references:
- kind: code
  role: implementation
  target: server/src/routes/calendars.ts
- kind: code
  role: implementation
  target: server/src/sync.ts
- kind: doc
  role: intent
  target: docs/settings/calendars.md
---

# Calendar

A calendar the family sees in Kinwall: one kept only in Kinwall, an ICS feed, or a Google, Outlook or CalDAV calendar synced both ways.

## Information kept

- **Name** — what it is called in Kinwall
- **Kind** — Kinwall only, ICS feed, Google, Outlook or CalDAV
- **Feed link** — the address of an ICS feed
- **Color** — the color its events fall back to when nobody is tagged
- **Members** — whose calendar it is; its events are tagged with them unless tagged otherwise
- **Default category** — the category its events get when no keyword matches and they have none of their own
- **Filter** — which of its events the family sees
- **Enabled** — when off, it stops syncing and its events are hidden
- **Wall screens and kids' devices can edit** — whether displays may add, change and delete its events (on to start)
- **Writable** — whether Kinwall can write its events back; ICS feeds never can
- **Last synced** — when it last synced
- **Sync status** — synced, never synced, or the last error in plain words
