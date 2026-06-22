# @chirag127/oriz-rate-limit

[![npm](https://img.shields.io/npm/v/@chirag127/oriz-rate-limit.svg)](https://www.npmjs.com/package/@chirag127/oriz-rate-limit)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

Per-user usage caps for Free/Pro/Max tiers (10/100/unlimited requests per day). Edge-friendly token bucket built on Cloudflare KV / Durable Objects.

## Install

```bash
pnpm add @chirag127/oriz-rate-limit
```

## Status

v0.1.0 is a slug-reservation stub. Real implementation lands when oriz apps consume it.

## Planned API

- `createLimiter({ tier, kv })` — token bucket factory bound to a Cloudflare KV namespace.
- `limiter.consume(userId, cost)` — returns `{ allowed, remaining, resetAt }`.
- Tiered defaults: Free = 10/day, Pro = 100/day, Max = unlimited.
- Durable Object backend for stronger consistency under burst load.
- Edge-compatible: zero Node-only deps, fits in Workers / Pages Functions.

## License

MIT (c) 2026 Chirag Singhal
