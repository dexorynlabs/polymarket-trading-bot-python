# Polymarket–Kalshi Arbitrage Bot

> Part of the [Polymarket Trading Bots](../README.md) pack · **Status: 🚧 in development**

Cross-venue arbitrage scanner and executor for **Polymarket** and **Kalshi**. The bot matches the same real-world event listed on both venues, pulls both order books, and reports price gaps after fees - then (optionally) executes both legs.

Both venues are regulated US markets with KYC. This bot does not bypass any of that; you need your own accounts.

## What it will do

1. **Event matching** - map a Polymarket market to its Kalshi counterpart (title, resolution date, outcome wording). This is the hard part and the main value of the repo.
2. **Spread scanner** - fetch both books, compute net edge after Polymarket and Kalshi fees, print a ranked table.
3. **Paper mode** - simulate both legs and log PnL, including resolution-rule mismatches (the real risk in this trade).
4. **Live mode** - gated behind an explicit flag with per-leg size caps.

## Release plan

| Layer | Needs keys? | Status |
|-------|-------------|--------|
| Scanner (public data) | No | 🚧 |
| Paper trading | No | planned |
| Live execution | Yes (both venues) | planned |

## Open vs. our live version

| In this repo | Kept private |
|--------------|--------------|
| Event matching, fee model, spread table | Latency stack and venue-specific execution tricks |
| Paper simulation and logs | Capital allocation across events |
| Gated live mode with caps | Resolution-risk filters tuned on our history |

Want the production build or custom work? [Telegram @dexoryn](https://t.me/dexoryn).

## Quick start

Coming with the first release. The folder will be self-contained: `requirements.txt`, `config.yaml.example`, and a `python -m` entry point.

---

← Back to the [bot pack](../README.md) · Follow [@Dexoryn](https://x.com/Dexoryn) for the launch post.
