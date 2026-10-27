# Hero Siege

Cooperative fantasy castle defence for up to four players, with an independent singleplayer mode.

The complete, tested release source (including `dist/`, assets, Node server, package lock and tests) is in **hero-siege-source.tar.gz**. Source is packaged because this repository is uploaded through GitHub's web interface. No credentials or installed dependencies are included.

## Run locally

```sh
tar -xzf hero-siege-source.tar.gz
npm ci
npm test
npm start
```

Open http://localhost:10000. Create a multiplayer room, share its six-character code, choose heroes and start as the host. The server simulates all players and sends shared world snapshots; skill upgrades, purchases and private warnings belong to individual players.

## Render

Node web service in Singapore. Build: `tar -xzf hero-siege-source.tar.gz && npm ci --omit=dev`. Start: `npm start`. HTTP readiness endpoint: `/health`. Default port 10000, bound to 0.0.0.0. No database or API key needed. Rooms are temporary; disconnection ends the session and server redeploys clear rooms.

Current testing configuration starts heroes at level 20 and prevents hero/tower damage. Existing game artwork and gameplay are included unchanged alongside the multiplayer integration.
