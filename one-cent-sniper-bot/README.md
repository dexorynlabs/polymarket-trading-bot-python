# Polymarket 1¢ Sniper Bot

> Part of the [Polymarket Trading Bots](../README.md) pack · **Status: 🚧 demo version planned**

A focused **Polymarket sniper bot** for long-shot outcomes: it scans order books for asks at or near the minimum tick (1¢), filters by liquidity and time-to-resolution, and places small, capped tail entries. One tactic, done cleanly.

## What the demo will include

- Book scanner for asks ≤ a configurable max price (default `0.01`–`0.02`)
- Filters: minimum ask size, market liquidity, hours to resolution, category blacklist
- Position caps per market and in total
- Dry-run by default; live orders gated by config
- Fill log with payoff tracking after resolution

## What stays private

Market-selection scoring and the timing model we use live. The demo picks by simple filters; the private version picks by expected value.

## Quick start

Coming with the first release. The folder will be self-contained: `requirements.txt`, `config.yaml.example`, and a `python -m` entry point.

---

← Back to the [bot pack](../README.md) · Launch post: [@Dexoryn](https://x.com/Dexoryn) · Questions: [Telegram @dexoryn](https://t.me/dexoryn).
