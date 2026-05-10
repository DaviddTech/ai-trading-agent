<div align="center">

# AI Trader MCP

### Build your own AI hedge fund with Claude, Codex, Cursor, and OpenClaw.

The agent-native skills directory for **Trader Dev MCP** — write Pine Script, backtest crypto strategies, optimize parameters, and run a full quant research desk from one conversation.

[![GitHub stars](https://img.shields.io/github/stars/DaviddTech/ai-trader-mcp?style=social)](https://github.com/DaviddTech/ai-trader-mcp/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/DaviddTech/ai-trader-mcp?style=social)](https://github.com/DaviddTech/ai-trader-mcp/network/members)
[![License: MIT](https://img.shields.io/github/license/DaviddTech/ai-trader-mcp)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/DaviddTech/ai-trader-mcp)](https://github.com/DaviddTech/ai-trader-mcp/commits/main)
[![MCP](https://img.shields.io/badge/MCP-Trader.dev-blue)](https://trader.dev/)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-compatible-7C3AED)](#-30-second-quickstart)
[![Codex](https://img.shields.io/badge/Codex-compatible-000000)](#-30-second-quickstart)
[![Cursor](https://img.shields.io/badge/Cursor-compatible-000000)](#-30-second-quickstart)
[![Pine Script](https://img.shields.io/badge/Pine%20Script-AI%20native-22C55E)](#-what-you-can-build)

**[Quickstart](#-30-second-quickstart)** · **[Skills](#-the-skills-directory)** · **[Examples](#-example-session)** · **[Roadmap](#-roadmap)** · **[Discord](#-community)** · **[YouTube](#-community)**

</div>

---

> ⚠️ **Research and education only.** AI Trader MCP does not place real trades, send real orders, or guarantee profits. Backtests are not future performance. Crypto trading is risky and leverage can cause catastrophic losses. Read [docs/DISCLAIMER.md](docs/DISCLAIMER.md) before doing anything.

---

<div align="center">

https://github.com/DaviddTech/ai-trading-agent/raw/main/assets/demo.mp4

*▶ Watch the AI hedge fund desk in action — 60 seconds.*

</div>

> *"Just like human traders have TradingView, AI agents need their own quant research desk."*

Most AI tools help traders write code. **AI Trader MCP helps AI agents run the entire research workflow** — generate hypotheses, write Pine Script, backtest, optimize, compare, and report. Built by [DaviddTech](https://davidd.tech), backtesting live on YouTube for 5+ years.

## ⚡ 30-second quickstart

<div align="center">

https://github.com/DaviddTech/ai-trading-agent/raw/main/assets/install.mp4

*▶ Full install walkthrough — under a minute.*

</div>

**1. Install Trader Dev MCP in your agent (pick one):**

```bash
# Claude Code
claude mcp add --transport sse --scope user trader-dev https://mcp.trader.dev/sse
```

```bash
# Codex
codex mcp add trader-dev -- npx -y mcp-remote https://mcp.trader.dev/sse
```

```text
# Cursor / OpenClaw / Cline / Continue / Windsurf / Gemini CLI
Register https://mcp.trader.dev/sse as a remote SSE MCP server.
```

**2. Paste this one-liner to your agent:**

```text
Read https://raw.githubusercontent.com/DaviddTech/ai-trader-mcp/main/SKILL.md
and help me build an AI hedge fund research desk using Trader Dev MCP.
```

**3. Ship your first backtest:**

```text
Backtest a Bollinger Band squeeze breakout on the top 10 Bybit pairs at 1h.
Report profit factor, max drawdown, and stability across symbols.
Reject overfit results.
```

That's it. Your agent is now a quant.

## 🔥 Why AI Trader MCP

| Without AI Trader MCP | With AI Trader MCP |
|---|---|
| Open TradingView, hand-code Pine Script, click backtest, copy results into a spreadsheet. | "Backtest this strategy on the top 10 Bybit pairs at 1h." Done in one message. |
| Click-optimize parameters one input at a time. | Parameter sweeps across stop loss, take profit, ATR multiples, regime filters — natural language. |
| Forget which version of a strategy worked last week. | Strategies live in Trader Dev. Fork, version, compare, promote, demote — all from chat. |
| Pay for a quant team. | Spin up a Mathematician, Mean-Reversion Engineer, Strategy Optimizer, and Position Optimizer — for free. |
| Wonder if your backtest is curve-fit. | Built-in robustness discipline: multi-pair, multi-timeframe, drawdown control, honest verdict labels. |
| Use AI to *write* code. | Use AI to *run the whole research desk.* |

## 🏭 Don't want to build your own strategies?

Not every trader wants to be a quant researcher. If you'd rather skip the research and run trading bots that already work, **[StrategyFactory.ai](https://strategyfactory.ai)** is where they live.

- **400+ trading bots** — every one **backtested *and* forward-tested with real-money live results**
- **No Pine Script knowledge required** — pick a bot, plug in, go
- **Real performance data** — not curve-fit screenshots, not "based on backtest" — actual live results
- **Plays nicely with this repo** — the AI Trader MCP skills can analyze, fork, and improve any Strategy Factory bot

| Path | What you do | Where to start |
|---|---|---|
| 🛠 **Build it yourself** | Use the skills, prompts, and loop roles in this repo. Pine Script + backtests + optimization, all from chat. | Stay here |
| 🚀 **Use what already works** | Browse the marketplace, pick a bot, plug into your trading stack. | [strategyfactory.ai](https://strategyfactory.ai) |

> **[→ Browse 400+ live-tested trading bots at StrategyFactory.ai →](https://strategyfactory.ai)**

## 🧠 The skills directory

Each skill is a focused, agent-readable `SKILL.md` that turns your AI client into a specialist on the desk.

| Skill | What it does |
|---|---|
| **[Main SKILL.md](SKILL.md)** | The entrypoint. Routes your agent into the right workflow. Start here. |
| **[AI Hedge Fund Manager](skills/ai-hedge-fund/SKILL.md)** | Coordinates the research desk. Picks specialists. Enforces discipline. |
| **[Quant Mathematician](skills/quant-mathematician/SKILL.md)** | Renaissance-style first-principles strategy creation. No retail indicator soup. |
| **[Mean Reversion Engineer](skills/mean-reversion-engineer/SKILL.md)** | Engineered mean-reversion systems for crypto. Volatility-aware, regime-filtered. |
| **[Strategy Optimizer](skills/strategy-optimizer/SKILL.md)** | Searches Trader Dev for existing strategies. Forks. Improves. Compares against baseline. |
| **[Position Optimizer](skills/position-optimizer/SKILL.md)** | Tests leverage, fractional Kelly, vol-targeting, drawdown throttling, bounded recovery. Keeps entries frozen. |

Plus copy-paste workflow prompts in [`prompts/`](prompts/) and [`examples/`](examples/).

## 🔁 The 24/7 desk — loop roles

One conversation. Fifteen specialists. Forever. **Every role is TradingView-native** — pure Pine Script and OHLCV, no off-chain data feeds.

Drop any of these into your AI client's `/loop` command and walk away. Each role fires every 15 minutes, runs one focused research cycle through Trader Dev MCP, and writes a structured report.

```bash
# Greenfield strategy creation, every 15 minutes
/loop 15m read loop/01-quant-mathematician.md and execute it

# Risk audits the existing book, every 15 minutes
/loop 15m read loop/08-risk-manager.md and execute it
```

| Category | Roles |
|---|---|
| 🎯 Coordination | [Hedge Fund Manager](loop/00-ai-hedge-fund-manager.md) |
| 🧮 Strategy creation | [Quant Mathematician](loop/01-quant-mathematician.md) · [Mean Reversion Engineer](loop/02-mean-reversion-engineer.md) · [Trend Following Engineer](loop/03-trend-following-engineer.md) · [Volatility Strategist](loop/04-volatility-strategist.md) · [Breakout Engineer](loop/05-breakout-engineer.md) |
| 🔧 Optimization | [Strategy Optimizer](loop/06-strategy-optimizer.md) · [Position Optimizer](loop/07-position-optimizer.md) |
| 🛡 Risk & robustness | [Risk Manager](loop/08-risk-manager.md) · [Drawdown Auditor](loop/09-drawdown-auditor.md) · [Overfitting Detector](loop/10-overfitting-detector.md) |
| 📐 Structural & pattern | [Multi-Timeframe Strategist](loop/11-multi-timeframe-strategist.md) · [Liquidity Sweep Hunter](loop/12-liquidity-sweep-hunter.md) · [Pattern Recognition Strategist](loop/14-pattern-recognition-strategist.md) |
| 🧪 Experimental | [Calendar & Lunar Cycle Strategist](loop/13-moon-phase-strategist.md) |

Full guide: [loop/README.md](loop/README.md).

## 📈 What you can build

- **An AI hedge fund research desk** — generate hypotheses → Pine Script → backtest → compare → report.
- **A Pine Script generator** — paste a strategy idea, get clean, no-repaint, no-lookahead Pine.
- **A TradingView backtest worker** — paste any Pine script, get a multi-pair, multi-timeframe robustness report.
- **A parameter optimizer** — sweep stops, TPs, ATR multiples, filters; reject overfits.
- **A position-sizing lab** — improve P&L by tuning leverage/Kelly/vol-targeting *without* changing entries.
- **A live signal monitor** — pipe Trader Dev signals to Telegram alerts.
- **A strategy fork-and-improve loop** — search the strategy library, fork winners, iterate one variable at a time.

## 🤖 Works with

<div align="center">

| ![Claude](https://img.shields.io/badge/Claude%20Code-7C3AED?logo=anthropic&logoColor=white) | ![Codex](https://img.shields.io/badge/Codex-000000?logo=openai&logoColor=white) | ![Cursor](https://img.shields.io/badge/Cursor-000000?logo=cursor&logoColor=white) | ![OpenClaw](https://img.shields.io/badge/OpenClaw-FF6B35) | ![Cline](https://img.shields.io/badge/Cline-1E40AF) | ![Continue](https://img.shields.io/badge/Continue-22C55E) | ![Windsurf](https://img.shields.io/badge/Windsurf-06B6D4) | ![Gemini](https://img.shields.io/badge/Gemini%20CLI-4285F4?logo=google&logoColor=white) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|

</div>

If your agent speaks MCP, AI Trader MCP works.

## 💬 Example session

```text
You:      I want to test a volatility breakout idea on crypto.
          Use the Quant Mathematician skill.

Agent:    Hypothesis: when realized volatility compresses below the
          20-period historical median for 8+ bars, a breakout in
          either direction has positive expectancy on 1h crypto.

          [writes Pine Script — no repaint, no lookahead]
          [calls mcp__trader-dev__run_backtest across 10 pairs × 4 timeframes]

          Results:
          Net profit:     +38.4%
          Profit factor:  1.62
          Max drawdown:   -14.1%
          Trades:         412
          Stable on 7/10 pairs across 1h, 2h, 4h.
          Fails on BTC and ETH — needs trend filter.

          Verdict: Incubate.
          Next iteration: add ADX < 25 regime filter.
```

*(Illustrative format. Numbers depend on your strategy, market, and assumptions.)*

## 🛠 Powered by Trader Dev MCP

[Trader Dev](https://trader.dev/) is the live MCP server doing the heavy lifting. Agents connected to it can:

- 🔍 `search_strategies` — discover proven strategy ideas
- ⚙️ `create_strategy` / `update_strategy` / `fork_strategy` — version your research
- 📊 `run_backtest` / `quick_backtest` — backtest Pine Script across crypto pairs
- 🎯 `optimize_strategy` — automated parameter sweeps
- 🔬 `compare_backtests` — diff versions side by side
- 📈 `get_equity_curve` / `get_trades` / `get_backtest_result` — pull granular metrics
- 📡 `get_recent_signals` / `list_active_alerts` / `test_telegram_sink` — live signal monitoring
- 💼 `promote_strategy` / `demote_strategy` — lifecycle management

Full tool reference: [docs/AGENT_GUIDE.md](docs/AGENT_GUIDE.md). Agents should always call `tools/list` first — never guess arguments.

## 🪙 Current market support

Trader Dev currently works on **crypto pairs**. The next markets unlock with stars:

- ⭐ 500 — more prompt packs and example Pine templates
- ⭐ 1,000 — public prompt leaderboard
- ⭐ 2,500 — downloadable Pine Script library
- ⭐ 5,000 — Forex data expansion begins
- ⭐ 10,000 — US stocks + futures research roadmap

If you want non-crypto markets, **[star this repo](https://github.com/DaviddTech/ai-trader-mcp)**.

## 🗺 Roadmap

**Live now**
- Trader Dev MCP server (SSE)
- Pine Script backtesting from any MCP-compatible agent
- Crypto pair coverage
- Parameter and position optimization workflows
- 5 specialist agent skills + prompt library
- Telegram alert workflows

**In progress**
- Native AI Trader alert system (less reliance on TradingView alerts)
- Backtest screenshots and shareable report cards pulled from the web app
- Downloadable Pine Scripts from the web app
- Risk Manager, PineScript Developer, Backtest Analyst, and Report Writer skills
- Walk-forward and Monte Carlo robustness checks

**Community-requested**
- Forex, stocks, futures
- More exchange data sources
- Strategy tournament leaderboards
- AI quant team presets by trading style

## 🧪 Research standards

This is not a hype trading bot. The skills are written to enforce:

- ✅ Robustness across symbols and nearby timeframes
- ✅ Drawdown control and profit factor over raw net profit
- ✅ Honest verdict labels — *Reject / Watchlist / Incubate / Candidate / Production candidate*
- ✅ No repainting, no lookahead, no future data
- ❌ No martingale without strict caps
- ❌ No one-coin cherry-picked backtests
- ❌ No hidden liquidation risk

## ⭐ Star history

[![Star History Chart](https://api.star-history.com/svg?repos=DaviddTech/ai-trader-mcp&type=Date)](https://star-history.com/#DaviddTech/ai-trader-mcp&Date)

If this repo saves you a single evening of manual backtesting, **[give it a star](https://github.com/DaviddTech/ai-trader-mcp)**. Stars unlock the roadmap above.

## 🤝 Contributing

Great contributions:

- New prompts and agent skills
- Pine Script strategy templates
- Backtest report formats
- Risk-management workflows
- Translations
- Demo videos and screenshots

See [CONTRIBUTING.md](CONTRIBUTING.md). Open an issue with [`Skill request`](.github/ISSUE_TEMPLATE/skill_request.md) or share a result with [`Backtest result`](.github/ISSUE_TEMPLATE/backtest_result.md).

## 👋 Community

- 🐦 **Twitter / X** — follow [@DaviddTech](https://twitter.com/DaviddTech) for new strategies and AI quant updates
- 🎥 **YouTube** — 5 years of live strategy backtesting on [DaviddTech](https://www.youtube.com/@DaviddTech)
- 🌐 **Website** — [davidd.tech](https://davidd.tech)
- 💬 **Discord** — *coming soon — watch the repo to be notified*

## ❓ FAQ

**Is this a trading bot?**
No. It is a skills directory that lets AI agents talk to the Trader Dev MCP server. Trader Dev runs the backtests; the skills tell your agent how to behave like a quant researcher.

**Does it place real trades?**
No. AI Trader MCP is for research, backtesting, and education. Live signals can be piped to Telegram, but execution is your responsibility.

**Which AI agents are supported?**
Anything that speaks MCP — Claude Code, Codex, Cursor, OpenClaw, Cline, Continue, Windsurf, Gemini CLI, and any custom agent using the [Model Context Protocol](https://modelcontextprotocol.io).

**Why Pine Script?**
Because TradingView is where most traders already live, and Pine Script is the fastest path from idea to backtest. Python/Polars support is on the roadmap.

**How is this different from `virattt/ai-hedge-fund`?**
That repo is a Python simulation of named-investor personas. AI Trader MCP is the **infrastructure layer** — an MCP server plus skills that any AI agent can use to actually generate, backtest, and optimize Pine Script strategies. They are complementary.

**Do I need a Trader Dev account?**
Some MCP tools require authentication. See [docs/QUICKSTART.md](docs/QUICKSTART.md).

**Will this make me money?**
No promises, no guarantees, no financial advice. See the disclaimer.

## 🛡 Risk notice

Trading is risky. Crypto is risky. Leverage is risky. Backtests are not guarantees. This project is for **research, backtesting, and education only**. Always paper trade and forward test before considering any live deployment. The authors and contributors accept no responsibility for losses. Full text: [docs/DISCLAIMER.md](docs/DISCLAIMER.md).

## 📄 License

MIT — see [LICENSE](LICENSE).

---

<div align="center">

**Built by [DaviddTech](https://davidd.tech) · Powered by [Trader Dev](https://trader.dev/)**

If AI agents should become real trading research assistants, **[star the repo ⭐](https://github.com/DaviddTech/ai-trader-mcp)**.

</div>
