# Pokémon Fusion Lab

React + TypeScript + Vite fan-project prototype. Select two Pokémon, tune anatomy and mutation level, generate a fusion, and save results in a local gallery.

## Development
```sh
npm install
npm run dev
```
The local Vite-only server does not serve `/api/generate`. Use `vercel dev` for full API testing.

## Image generation setup
Create a Venice API key and add `VENICE_API_KEY` as a server-side environment variable in your Vercel project. Optionally configure `VENICE_IMAGE_MODEL` (defaults to `grok-imagine-image`). Redeploy. API credits are charged per generation. The provider can reject images. **There is no durable rate limit or account authentication in this prototype. Do not publicly expose a paid API key without adding durable server-side quotas and authentication.**

## Persistence
Generated images are stored locally in browser IndexedDB, not synced between devices. Download images to preserve them. Future upgrades: cloud gallery, authentication, mutations using reference-image editing, and spending caps.

Pokémon selection/artwork supplied by PokéAPI and its sprite repository. Unofficial fan experiment; Pokémon rights belong to their respective owners.
