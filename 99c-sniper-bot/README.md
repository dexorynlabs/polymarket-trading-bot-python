# Polymarket 99¢ Sniper Bot (End-Cycle Sniper)

> Part of the [Polymarket Trading Bots](../README.md) pack · **Status: 🚧 demo version planned**

Also known as the **end-cycle sniper**, **reverse hunting bot**, or **99-cent strategy bot**: it buys near-certain outcomes at 97–99¢ in the final hours before resolution and harvests the last few cents when the market settles at $1.00. The mirror image of the [1¢ Sniper Bot](../1c-sniper-bot/) - many small wins instead of many small losses.

The catch is obvious once you run it: one wrong resolution or UMA dispute erases 30+ winning trades. Resolution-risk filtering *is* the strategy.

## What the demo will include

- Scanner for outcomes trading ≥ a configurable floor (default `0.97`) with ≤ N hours to resolution
- Filters: market liquidity, minimum ask size, category whitelist, hours-to-resolution window
- Position caps per market and in total, plus a max-concurrent-markets limit
- Dry-run by default; live orders gated by config
- Fill log with realised yield per market and per week after resolution

## What stays private

| In this repo | Our live version |
|--------------|------------------|
| Price + time-to-resolution filters | Resolution / dispute-risk scoring per market and resolver |
| Static category whitelist | Learned blacklist from our dispute history |
| Equal sizing with caps | Sizing by expected yield vs. tail risk |

The demo shows the mechanics of the 99¢ trade; the private version decides *which* 99¢ markets are actually 99%.

## Quick start

Coming with the first release. The folder will be self-contained: `requirements.txt`, `config.yaml.example`, and a `python -m` entry point.

---

← Back to the [bot pack](../README.md) · Pair it with the [1¢ Sniper Bot](../1c-sniper-bot/) · Launch post: [@Dexoryn](https://x.com/Dexoryn) · Questions: [Telegram @dexoryn](https://t.me/dexoryn).
