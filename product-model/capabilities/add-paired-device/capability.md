---
availability:
- place: web-app::welcome
- place: web-app::administration
domain: access
references:
- kind: code
  role: implementation
  target: server/src/routes/pair.ts
- kind: code
  role: implementation
  target: server/src/auth.ts#deviceKindOwner
- kind: code
  role: implementation
  target: web/src/App.tsx#DisplayPairing
- kind: code
  role: implementation
  target: web/src/Settings.tsx#DisplaysSection
- kind: doc
  role: intent
  target: docs/getting-started/put-it-on-the-wall.md
---

# Add a wall screen or kid's device

Join a wall screen or a kid's tablet or phone to the family: the screen shows a code, and a parent approves it from their own device. A wall screen shows the whole family; a kid's device shows only that kid's things.
