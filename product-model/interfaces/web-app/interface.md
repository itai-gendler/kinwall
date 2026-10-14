---
type: web
actors:
- parent
- kid
- wall-screen
entryPoints:
- web: /#/home
references:
- kind: code
  role: implementation
  target: web/src/App.tsx
- kind: doc
  role: intent
  target: docs/getting-started/put-it-on-the-wall.md
---

# Kinwall app

The touch app the family uses on the wall screen, tablets, phones and computers, added to the home screen or opened in a browser. Parents' phones and
computers sign in with a passkey; wall screens and kids' devices pair with a code.

## Intent

One app for every screen in the house, readable from across the room on the wall and usable by kids.
