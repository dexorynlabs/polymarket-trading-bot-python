# Polymarket Trading Bots | Kalshi Arbitrage · Market Maker · Copy Trading

**Languages:** [English](README.md) · [中文](public/README.zh-CN.md) · [Русский](public/README.ru.md)

> **One repo, five Polymarket bots - built and operated by a team running live market-making on Polymarket.**
> **Open-source cores • Paper/dry-run first • Real on-chain execution • Python**

> **Need help or a production build?**
> 📱 **Telegram**: [t.me/dexoryn](https://t.me/dexoryn) | 🎮 **Discord**: `dexoryn_` | 🐦 **X**: [@Dexoryn](https://x.com/Dexoryn)

---

## 🤖 The bots

| Bot | Status | What it does | Folder |
|-----|--------|--------------|--------|
| **Copy Trading Bot** | ✅ Live-tested, open source | Mirrors leader wallets in real time - multi-wallet, predictions & perps, web dashboard | [`copy-trading-bot/`](copy-trading-bot/) |
| **Polymarket ↔ Kalshi Arbitrage Bot** | 🚧 In development | Matches the same event on both venues and surfaces price gaps after fees | [`kalshi-arbitrage-bot/`](kalshi-arbitrage-bot/) |
| **Market Maker Bot** | 🚧 Demo version planned | Two-sided quoting with inventory limits - reference implementation of our live MM desk | [`market-maker-bot/`](market-maker-bot/) |
| **1¢ Sniper Bot** | 🚧 Demo version planned | Scans books for near-zero asks on long-shot outcomes and sizes small tail entries | [`1c-sniper-bot/`](1c-sniper-bot/) |
| **99¢ Sniper Bot** | 🚧 Demo version planned | End-cycle sniper: buys near-certain outcomes at 97–99¢ before resolution to harvest the final cents | [`99c-sniper-bot/`](99c-sniper-bot/) |

**Start here:** the copy trading bot is the finished product. The other four are being released one at a time - watch the repo or follow [@Dexoryn](https://x.com/Dexoryn) for each launch.

Dedicated copy-trading repos: [English](https://github.com/dexorynlabs/polymarket-copy-trading-bot) · [中文](https://github.com/dexoryn-china/polymarket-copy-trading-bot)

---

## 🎥 Live execution proof (copy trading bot)

Real on-chain runs from the copy bot in this repo - not simulations.

https://github.com/user-attachments/assets/2194ef92-b0f7-40e1-9835-4d2965e85e81

- **+$80 in ~15 minutes**, bot ran unattended
- A second session the next day added **+$230** - same code, separate run

<p align="center">
  <img src="public/Realtradehistory/securebet.jpg" alt="Copy trading PnL: bot wallet vs securebet target - matching chart shape" width="100%"/>
</p>

Bot wallet (left) vs. the copied trader (right): the **same equity-curve shape** for the day. Full videos, stories, and setup are in [`copy-trading-bot/README.md`](copy-trading-bot/README.md).

---

## 🚀 Quick start (copy trading bot)

```bash
git clone https://github.com/dexorynlabs/polymarket-trading-bots.git
cd polymarket-trading-bots/copy-trading-bot

pip install -r requirements.txt
cp config.yaml.example config.yaml   # keep mode: dry_run for the first run

python -m app.main
# dashboard → http://127.0.0.1:8787
```

Each bot folder is self-contained with its own README, requirements, and config. Nothing here runs with real funds until you explicitly switch it to `real` / live mode.

---

## 🛡 Safety

- Every bot ships **paper / dry-run first**; live mode is opt-in
- Use a dedicated wallet with limited balance
- Never commit `config.yaml`, keys, or API credentials
- Past results do not guarantee future results

---

## 👤 Author & Contact

**Dexoryn Labs** - Polymarket trading automation. We run market-making and execution bots on Polymarket every day; the open-source versions here are the cores we're comfortable publishing.

- **Telegram**: [@dexoryn](https://t.me/dexoryn) (fastest)
- **X**: [@Dexoryn](https://x.com/Dexoryn)
- **Discord**: `dexoryn_`
- **GitHub**: [@dexorynLabs](https://github.com/dexorynLabs)
- **WeChat**: scan to add **DexorynWe**

<p align="center">
  <img src="public/dexoryn_tg.jpg" alt="Telegram QR code - @dexoryn" height="260"/>
  &nbsp;&nbsp;
  <img src="public/dexoryn_wechat.png" alt="WeChat QR code - DexorynWe" height="260"/>
</p>

---

## Contributing

See [CONTRIBUTING.md](.github/CONTRIBUTING.md). Community: [Code of Conduct](.github/CODE_OF_CONDUCT.md) · [Security](.github/SECURITY.md) · [MIT License](LICENSE)

## Legal Disclaimer

Trading on Polymarket and Kalshi involves **substantial risk of loss**. Dexoryn is not responsible for losses from using this software. You are solely responsible for wallet security, configuration, and capital at risk.

**Only trade with funds you can afford to lose.**

Questions: [@dexoryn](https://t.me/dexoryn) · ⭐ star the repo if it helps.
