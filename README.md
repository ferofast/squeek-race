# Squeek Race

Predict the Squeekchain hamster's next round. A Genesis Code project for
Squeekchain (squeekchain.com/genesis/code).

## Play it live

https://muse.ai/s/hamster-round-prediction-game-xhf6hexdav5od/9kKPvJ-dL6CPvhpUEFgT6vL3nl-mhZx6b5HTgXiWZf0

## How it works

Every Squeekchain round settles on-chain with a work total. Before the next
settlement lands, call **Higher** or **Lower**: will the next settled round
add more or less work than the last one?

- **Live mode** — locks your call and resolves it when the next real
  settlement arrives on Sepolia (polls the public API every 30 s).
- **Blitz mode** — instantly replays real past settlements, so the game stays
  playable while the hamster sleeps.
- Points, streaks, a session scoreboard, a work-per-settlement chart, and a
  live stat rail (hamster state/speed, lifetime distance, current round,
  SQK in circulation vs the 2.1B cap).

## Live data

All data comes from the public Squeekchain API (`https://api.squeekchain.com`,
no key, CORS `*`):

- `GET /v1/status` — live measurement (distance, speed, rpm, core status)
  and the settled-through round.
- `GET /v1/settlements` — recent settlements with work added per round.
- `GET /v1/economy/state` — current round, supply, staking, NFT stats.

No data is invented. This is Sepolia testnet data.

## Run it

Open `index.html` in a browser. No build step, no keys, no wallet needed.

## Squeekchain Genesis Code

squeekchain-project: f74e971e-85e7-417c-ace3-10f588ba7ada
