---
scope: 'Kinwall''s server and web app for the core household areas: signing in and pairing devices, family members and settings, calendars and events, chores
  with points and rewards, and lists.'
method: Static reading of the server routes, auth rules, sync and web screens at the pinned commit, with the docs as leads; nothing was executed.
covered:
- description: Sign-in, setup, pairing, passkey, recovery-code, device-key and security-log routes and the access rules
  paths:
  - server/src/auth.ts
  - server/src/routes/setup.ts
  - server/src/routes/pair.ts
  - server/src/routes/passkeys.ts
  - server/src/routes/recovery.ts
  - server/src/routes/keys.ts
  - server/src/routes/security-events.ts
  - server/src/routes/me.ts
  - server/src/webauthn.ts
- description: Family member, category and household settings routes
  paths:
  - server/src/routes/members.ts
  - server/src/routes/categories.ts
  - server/src/routes/settings.ts
  - server/src/calendar-categories.ts
- description: Calendar, account, event and sync code with the calendar providers
  paths:
  - server/src/routes/calendars.ts
  - server/src/routes/accounts.ts
  - server/src/routes/oauth.ts
  - server/src/routes/events.ts
  - server/src/routes/providers.ts
  - server/src/sync.ts
  - server/src/providers/
  - server/src/calendar-filter.ts
  - server/src/calendar-members.ts
  - server/src/default-calendar.ts
  - server/src/recurrence.ts
  - server/src/event-id.ts
- description: Chore, approval, chore idea, bonus point and leaderboard routes
  paths:
  - server/src/routes/chores.ts
  - server/src/routes/chore-suggestions.ts
  - server/src/routes/bonus-points.ts
  - server/src/routes/leaderboard.ts
- description: Reward and reward request routes
  paths:
  - server/src/routes/rewards.ts
- description: List and list item routes with remembered item places
  paths:
  - server/src/routes/lists.ts
  - server/src/item-memory.ts
- description: Board data route
  paths:
  - server/src/routes/snapshot.ts
- description: Web screens for the Board, calendar, chores, rewards, lists, settings, setup and pairing
  paths:
  - web/src/App.tsx
  - web/src/Board.tsx
  - web/src/Calendar.tsx
  - web/src/Chores.tsx
  - web/src/ChoreSuggest.tsx
  - web/src/GivePoints.tsx
  - web/src/Rewards.tsx
  - web/src/Lists.tsx
  - web/src/GetStuffDone.tsx
  - web/src/Settings.tsx
  - web/src/Setup.tsx
  - web/src/SecurityActivitySheet.tsx
  - web/src/outbox.ts
  - web/src/trip.ts
- description: Database schema of the mapped areas
  paths:
  - server/migrations/
exclusions:
- description: Build, release, CI and deployment configuration
  paths:
  - .github/
  - Dockerfile
  - docker-compose.yml
  - docker-entrypoint.sh
  - wrangler.toml
  - scripts/
  - release-please-config.json
  - web/scripts/
- description: Server hosting entry points and database adapters
  paths:
  - server/src/node.ts
  - server/src/worker.ts
  - server/src/entry.ts
  - server/src/d1-sqlite.ts
  - server/src/db.ts
  - server/src/migrate.ts
  - server/src/worker-migrations.ts
- description: Server and web tests
  paths:
  - server/test/
  - web/test/
- description: Health check, media tokens and the change poll
  paths:
  - server/src/routes/health.ts
  - server/src/routes/media.ts
  - server/src/routes/rev.ts
- description: Fonts, styles, screenshots, demo drawings and the demo build data
  paths:
  - web/src/fonts/
  - web/src/styles.css
  - docs/screenshots/
  - web/demo-drawings/
  - web/src/mock.ts
unmapped:
- description: Meals, recipes, restaurant nights and orders
  paths:
  - server/src/routes/meals.ts
  - server/src/routes/recipe-share.ts
  - server/src/routes/restaurants.ts
  - server/src/meals.ts
  - server/src/recipe-web.ts
  - server/src/restaurant-import.ts
  - web/src/Meals.tsx
- description: Medications, refills and health and reading trackers
  paths:
  - server/src/routes/medications.ts
  - server/src/routes/medication-refills.ts
  - server/src/routes/trackers.ts
  - server/src/routes/books.ts
  - server/src/routes/library.ts
- description: Check-ins, Temp check, journals, insights and the energy battery
  paths:
  - server/src/routes/check-in.ts
  - server/src/routes/temp-check.ts
  - server/src/routes/journal.ts
  - server/src/routes/insights.ts
  - server/src/battery.ts
  - server/src/insights.ts
- description: Push notifications, reminders, transition warnings and Live Activities
  paths:
  - server/src/routes/push.ts
  - server/src/routes/live-activities.ts
  - server/src/notify.ts
  - server/src/webpush.ts
  - server/src/nudges.ts
  - server/src/apns.ts
- description: Newscast, polls, outings, contacts and discussion notes
  paths:
  - server/src/routes/newscast.ts
  - server/src/routes/polls.ts
  - server/src/routes/outings.ts
  - server/src/routes/outing-feeds.ts
  - server/src/routes/contacts.ts
  - server/src/routes/notes.ts
- description: Photos, Google Photos, the photo folder, stickers and sandboxed activities
  paths:
  - server/src/routes/photos.ts
  - server/src/routes/google-photos.ts
  - server/src/routes/photo-folder.ts
  - server/src/routes/stickers.ts
  - server/src/routes/plugins.ts
- description: Chore library and activity chores
  paths:
  - server/src/routes/chore-library.ts
- description: REST API docs, MCP server, connected apps, API keys and webhooks
  paths:
  - server/src/mcp.ts
  - server/src/routes/mcp-oauth.ts
  - server/src/routes/webhooks.ts
  - server/src/bus.ts
- description: Export and import of the family data
  paths:
  - server/src/routes/data.ts
- description: The Add to Kinwall share shortcut
  paths:
  - server/src/routes/share.ts
- description: Appearance, night screen, quiet PIN, weather, quotes and facts and profile stats
  paths:
  - server/src/routes/appearance.ts
  - server/src/routes/night-screen.ts
  - server/src/routes/quiet-pin.ts
  - server/src/routes/weather.ts
  - server/src/routes/tidbits.ts
  - server/src/routes/member-stats.ts
limitations: []
---

# Coverage
