# Торговые боты Polymarket | Арбитраж с Kalshi · Маркет-мейкер · Копи-трейдинг

**Языки:** [English](../README.md) · [中文](README.zh-CN.md) · [Русский](README.ru.md)

> **Один репозиторий, четыре бота для Polymarket - от команды, которая ежедневно делает маркет-мейкинг на Polymarket в live.**
> **Открытое ядро • Сначала paper / dry-run • Реальное исполнение on-chain • Python**

> **Нужна помощь или production-сборка?**
> 📱 **Telegram**: [t.me/dexoryn](https://t.me/dexoryn) | 🎮 **Discord**: `dexoryn_` | 🐦 **X**: [@Dexoryn](https://x.com/Dexoryn)

---

## 🤖 Боты

| Бот | Статус | Что делает | Папка |
|-----|--------|------------|-------|
| **Копи-трейдинг бот** | ✅ Проверен в live, open source | Зеркалит кошельки лидеров в реальном времени - несколько кошельков, predictions & perps, web-дашборд | [`copy-trading-bot/`](../copy-trading-bot/) |
| **Арбитраж Polymarket ↔ Kalshi** | 🚧 В разработке | Сопоставляет одно событие на двух площадках и показывает разницу цен после комиссий | [`kalshi-arbitrage-bot/`](../kalshi-arbitrage-bot/) |
| **Маркет-мейкер** | 🚧 Демо-версия в планах | Двусторонние котировки с лимитами по инвентарю - референс нашего live MM | [`market-maker-bot/`](../market-maker-bot/) |
| **1¢ снайпер** | 🚧 Демо-версия в планах | Ищет аски около минимального тика на маловероятных исходах и ставит небольшие хвостовые позиции | [`one-cent-sniper-bot/`](../one-cent-sniper-bot/) |

**Начните отсюда:** копи-трейдинг бот - готовый продукт. Остальные три выходят по одному - следите за репозиторием или [@Dexoryn](https://x.com/Dexoryn).

Отдельные репозитории копи-трейдинга: [English](https://github.com/dexorynlabs/polymarket-copy-trading-bot) · [中文](https://github.com/dexoryn-china/polymarket-copy-trading-bot)

---

## 🎥 Доказательство live-исполнения (копи-трейдинг бот)

Реальные on-chain запуски бота из этого репозитория - не симуляция.

https://github.com/user-attachments/assets/2194ef92-b0f7-40e1-9835-4d2965e85e81

- **+$80 за ~15 минут**, бот работал без присмотра
- Вторая сессия на следующий день добавила **+$230** - тот же код, отдельный запуск

<p align="center">
  <img src="Realtradehistory/securebet.jpg" alt="PnL копи-трейдинга: кошелёк бота vs securebet - совпадение формы графика" width="100%"/>
</p>

Кошелёк бота (слева) и копируемый трейдер (справа): **одинаковая форма кривой** за день. Полные видео, истории и настройка - в [`copy-trading-bot/public/README.ru.md`](../copy-trading-bot/public/README.ru.md).

---

## 🚀 Быстрый старт (копи-трейдинг бот)

```bash
git clone https://github.com/dexorynlabs/polymarket-trading-bots.git
cd polymarket-trading-bots/copy-trading-bot

pip install -r requirements.txt
cp config.yaml.example config.yaml   # для первого запуска оставьте mode: dry_run

python -m app.main
# дашборд → http://127.0.0.1:8787
```

Каждая папка бота самодостаточна: свой README, зависимости и конфиг. Ничего не торгует реальными средствами, пока вы явно не включите `real` / live режим.

---

## 🛡 Безопасность

- Все боты поставляются в режиме **paper / dry-run**; live включается вручную
- Используйте отдельный кошелёк с ограниченным балансом
- Никогда не коммитьте `config.yaml`, ключи или API-креды
- Прошлые результаты не гарантируют будущих

---

## 👤 Автор и контакты

**Dexoryn Labs** - автоматизация торговли на Polymarket. Мы ежедневно запускаем маркет-мейкинг и исполняющих ботов на Polymarket; здесь открыты те ядра, которые мы готовы публиковать.

- **Telegram**: [@dexoryn](https://t.me/dexoryn) (быстрее всего)
- **X**: [@Dexoryn](https://x.com/Dexoryn)
- **Discord**: `dexoryn_`
- **GitHub**: [@dexorynLabs](https://github.com/dexorynLabs)
- **WeChat**: отсканируйте, чтобы добавить **DexorynWe**

<p align="center">
  <img src="dexoryn_tg.jpg" alt="QR Telegram - @dexoryn" height="260"/>
  &nbsp;&nbsp;
  <img src="dexoryn_wechat.png" alt="QR WeChat - DexorynWe" height="260"/>
</p>

---

## Участие

См. [CONTRIBUTING.md](../.github/CONTRIBUTING.md). Сообщество: [Code of Conduct](../.github/CODE_OF_CONDUCT.md) · [Security](../.github/SECURITY.md) · [MIT License](../LICENSE)

## Отказ от ответственности

Торговля на Polymarket и Kalshi сопряжена с **существенным риском убытков**. Dexoryn не несёт ответственности за потери от использования этого ПО. Вы отвечаете за безопасность кошелька, конфигурацию и капитал.

**Торгуйте только теми средствами, которые готовы потерять.**

Вопросы: [@dexoryn](https://t.me/dexoryn) · ⭐ поставьте звезду, если репозиторий полезен.
