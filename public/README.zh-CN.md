# Polymarket 交易机器人合集 | Kalshi 套利 · 做市 · 跟单

**语言：** [English](../README.md) · [中文](README.zh-CN.md) · [Русский](README.ru.md)

> **一个仓库，五个 Polymarket 机器人 — 由每天在 Polymarket 上实盘做市的团队构建与运营。**
> **开源核心 • 默认模拟/干跑 • 真实链上执行 • Python**

> **需要帮助或生产版本？**
> 📱 **Telegram**：[t.me/dexoryn](https://t.me/dexoryn) | 🎮 **Discord**：`dexoryn_` | 🐦 **X**：[@Dexoryn](https://x.com/Dexoryn)

---

## 🤖 机器人列表

| 机器人 | 状态 | 功能 | 目录 |
|--------|------|------|------|
| **跟单机器人** | ✅ 实盘验证，已开源 | 实时镜像领头钱包 — 多钱包、预测市场与永续、Web 仪表盘 | [`copy-trading-bot/`](../copy-trading-bot/) |
| **Polymarket ↔ Kalshi 套利机器人** | 🚧 开发中 | 匹配两个平台上的同一事件，计算扣费后的价差 | [`kalshi-arbitrage-bot/`](../kalshi-arbitrage-bot/) |
| **做市机器人** | 🚧 演示版计划中 | 双边报价 + 库存限制 — 我们实盘做市系统的参考实现 | [`market-maker-bot/`](../market-maker-bot/) |
| **1 美分狙击机器人** | 🚧 演示版计划中 | 扫描冷门结果的极低价卖单，小仓位尾部入场 | [`1c-sniper-bot/`](../1c-sniper-bot/) |
| **99 美分狙击机器人** | 🚧 演示版计划中 | 周期末狙击：在结算前以 97–99 美分买入近乎确定的结果，收割最后几美分 | [`99c-sniper-bot/`](../99c-sniper-bot/) |

**从这里开始：** 跟单机器人是已完成的产品，其余四个将逐个发布 — 关注本仓库或 [@Dexoryn](https://x.com/Dexoryn) 获取每次发布。

独立跟单仓库：[中文版](https://github.com/dexoryn-china/polymarket-copy-trading-bot) · [English](https://github.com/dexorynlabs/polymarket-copy-trading-bot)

---

## 🎥 实盘执行证明（跟单机器人）

来自本仓库跟单机器人的真实链上运行 — 非模拟。

https://github.com/user-attachments/assets/2194ef92-b0f7-40e1-9835-4d2965e85e81

- **约 15 分钟 +$80**，机器人无人值守运行
- 次日第二次会话再 **+$230** — 同一代码，独立运行

<p align="center">
  <img src="Realtradehistory/securebet.jpg" alt="跟单盈亏：机器人钱包 vs securebet 目标 - 曲线形状一致" width="100%"/>
</p>

机器人钱包（左）与被跟单交易者（右）：当日**相同的权益曲线形状**。完整视频、故事与配置见 [`copy-trading-bot/public/README.zh-CN.md`](../copy-trading-bot/public/README.zh-CN.md)。

---

## 🚀 快速开始（跟单机器人）

```bash
git clone https://github.com/dexorynlabs/polymarket-trading-bots.git
cd polymarket-trading-bots/copy-trading-bot

pip install -r requirements.txt
cp config.yaml.example config.yaml   # 首次运行保持 mode: dry_run

python -m app.main
# 仪表盘 → http://127.0.0.1:8787
```

每个机器人目录自包含：各自的 README、依赖与配置。在你明确切换为 `real` / 实盘模式之前，不会动用真实资金。

---

## 🛡 安全

- 所有机器人**默认模拟/干跑**，实盘需手动开启
- 使用余额有限的专用钱包
- 切勿提交 `config.yaml`、私钥或 API 凭证
- 过往表现不代表未来结果

---

## 👤 作者与联系

**Dexoryn Labs** — Polymarket 交易自动化。我们每天在 Polymarket 上运行做市与执行机器人；这里开源的是我们愿意公开的核心部分。

- **Telegram**：[@dexoryn](https://t.me/dexoryn)（回复最快）
- **X**：[@Dexoryn](https://x.com/Dexoryn)
- **Discord**：`dexoryn_`
- **GitHub**：[@dexorynLabs](https://github.com/dexorynLabs)
- **微信**：扫码添加 **DexorynWe**

<p align="center">
  <img src="dexoryn_tg.jpg" alt="Telegram 二维码 - @dexoryn" height="260"/>
  &nbsp;&nbsp;
  <img src="dexoryn_wechat.png" alt="微信二维码 - DexorynWe" height="260"/>
</p>

---

## 贡献

详见 [CONTRIBUTING.md](../.github/CONTRIBUTING.md)。社区：[行为准则](../.github/CODE_OF_CONDUCT.md) · [安全](../.github/SECURITY.md) · [MIT 许可证](../LICENSE)

## 法律声明

在 Polymarket 与 Kalshi 交易存在**重大亏损风险**。Dexoryn 不对使用本软件造成的损失负责。钱包安全、配置与资金风险由您自行承担。

**请仅使用您能承受损失的资金进行交易。**

问题咨询：[@dexoryn](https://t.me/dexoryn) · 有帮助请 ⭐ Star。
