# Contributing

Thanks for helping improve this project. Issues and pull requests are welcome.

## Before you start

- Read the [README](../README.md) for the bot list and safety notes.
- **Never commit secrets** - `config.yaml`, `targets.yaml`, `settings.yaml`, wallet keys, or API credentials.
- Trading bots carry financial risk. Test in `dry_run` / paper mode before suggesting changes that affect live execution.

## Repository layout

This is a monorepo. Each bot lives in its own self-contained folder with its own README, `requirements.txt`, config example, and tests:

| Folder | Bot |
|--------|-----|
| `copy-trading-bot/` | Copy trading bot (canonical repo: [polymarket-copy-trading-bot](https://github.com/dexorynlabs/polymarket-copy-trading-bot)) |
| `kalshi-arbitrage-bot/` | Polymarket ↔ Kalshi arbitrage bot |
| `market-maker-bot/` | Market maker bot (demo) |
| `1c-sniper-bot/` | 1¢ sniper bot (demo) |
| `99c-sniper-bot/` | 99¢ / end-cycle sniper bot (demo) |

Bots do not import from each other. Keep changes inside one bot folder per PR.

## Development setup

```bash
git clone https://github.com/dexorynlabs/polymarket-trading-bots.git
cd polymarket-trading-bots/<bot-folder>

pip install -r requirements.txt
pip install -r requirements-dev.txt   # if present

cp config.yaml.example config.yaml
pytest
```

Optional UI work for the copy bot: see [`copy-trading-bot/ui/README.md`](../copy-trading-bot/ui/README.md).

## Pull requests

1. Fork the repo and create a branch from `main` (e.g. `feature/short-description`).
2. Keep changes focused - one logical change per PR when possible.
3. Run tests inside the bot folder you changed: `pytest`
4. Open a PR with a clear summary and test notes.

Commit messages in this repo typically use prefixes like `feat:`, `fix:`, `docs:`, `test:`, or `perf:`.

## Code of conduct

This project follows the [Code of Conduct](CODE_OF_CONDUCT.md). Be respectful in issues and reviews.

## Questions

- **Telegram**: [@dexoryn](https://t.me/dexoryn)
- **GitHub Issues**: for bugs and feature requests (no secrets in issue text)
