# AGENTS.md

## Architecture

- `index.html` holds the whole app: styles in `<style>`, logic in one IIFE `<script>`. There is no build step and no dependencies.
- `netlify.toml` publishes the repository root as a static site.

## Key sections in the script

- Auth store: `localStorage` keys `arcade_users_v1` and `arcade_session_v1`. This is a demo; the password hash isn't secure.
- Catalog: the `allGames` array. Entries with `playable: true` have a working game. The rest show "coming soon".
- Each game has its own state object plus `reset*`, `update*` and `draw*` functions, which are wired into `gameLoop`, `drawCurrentGame`, `resetCurrentGame`, `updateStatsUI` and the key handlers.
- `BADGES` and `AVATARS` set up the progression and the shop.

## Conventions and decisions

- The owner asked for the page to be published exactly as provided. Don't change content or behavior unless asked.
- Whenever server-side persistence or real auth gets added, use Netlify platform primitives (Netlify Identity, Netlify Database).
