# 🔁 Loop Roles — The AI Hedge Fund Desk

This is the **24/7 quant research desk** for AI Trader MCP. Each file in this folder is a self-contained agent prompt designed to be fired on a recurring 15-minute interval using your AI client's `/loop` command (Claude Code, Codex, etc.) connected to the [Trader Dev MCP server](https://mcp.trader.dev/sse).

> **One conversation. Fifteen specialists. Forever.**
>
> Open Claude Code. Run `/loop 15m read loop/01-quant-mathematician.md` (or any other role). Walk away. Come back to a stack of fresh research reports, backtested strategies, fork comparisons, and risk audits.

## ⚠️ Hard rule — TradingView-native only

Every strategy this desk creates must be backtestable on **TradingView using Pine Script and OHLCV data alone**.

The desk does not have access to:

- ❌ Real-time funding rates (not in TradingView)
- ❌ Cross-exchange arbitrage data
- ❌ Sentiment feeds (Fear & Greed indices, social-media volume)
- ❌ Off-chain on-chain analytics (Glassnode, IntoTheBlock-style data)
- ❌ Options flow, dealer positioning, gamma exposure
- ❌ Order book depth or liquidations from off-exchange data sources
- ❌ Anything that requires a custom data feed

The desk **does** have access to:

- ✅ OHLCV from any TradingView symbol (via `request.security`)
- ✅ Volume
- ✅ All built-in Pine Script TA functions
- ✅ Multiple timeframes (`request.security` with `lookahead=barmerge.lookahead_off`)
- ✅ Multiple symbols (BTC vs ETH ratio is doable)
- ✅ Date / time math (sessions, days, halving cycles, lunar phase via math)
- ✅ Volatility, range, ATR-based logic
- ✅ Pivots, swing highs/lows, Donchian, Bollinger, Keltner
- ✅ Anything you can compute from the chart itself

If a role wants data not on this list, the role is wrong for this desk. Roles must be redesigned around price-action equivalents.

## How the loop works

The `/loop` command in Claude Code, Codex, and compatible agents fires the same prompt on a fixed cadence. Each fire is a fresh research cycle — no context carry-over guaranteed, so every role file is self-contained and produces a single, complete research report per cycle.

### Quickstart

```bash
# Pick a role and start it on a 15-minute loop
/loop 15m read loop/01-quant-mathematician.md and execute it

# Or run several in parallel from different chat tabs:
# Tab 1 — strategy creation
/loop 15m read loop/02-mean-reversion-engineer.md and execute it
# Tab 2 — optimization
/loop 15m read loop/06-strategy-optimizer.md and execute it
# Tab 3 — risk audit
/loop 15m read loop/08-risk-manager.md and execute it
```

### Self-pacing variant

Omit the interval to let the agent self-pace based on workload:

```bash
/loop read loop/00-ai-hedge-fund-manager.md and execute it
```

## The desk

### 🎯 Coordination
| File | Role | What it does each cycle |
|---|---|---|
| [00-ai-hedge-fund-manager.md](00-ai-hedge-fund-manager.md) | Hedge Fund Manager | Surveys the desk, picks the next priority job, dispatches summary report. |

### 🧮 Strategy creation (TradingView-native)
| File | Role | What it does each cycle |
|---|---|---|
| [01-quant-mathematician.md](01-quant-mathematician.md) | Quant Mathematician | First-principles strategy ideation + Pine Script + backtest. |
| [02-mean-reversion-engineer.md](02-mean-reversion-engineer.md) | Mean Reversion Engineer | Engineered reversion systems, no RSI/BB indicator soup. |
| [03-trend-following-engineer.md](03-trend-following-engineer.md) | Trend Following Engineer | Robust trend systems with regime filters. |
| [04-volatility-strategist.md](04-volatility-strategist.md) | Volatility Strategist | Vol compression / expansion / clustering edges. |
| [05-breakout-engineer.md](05-breakout-engineer.md) | Breakout Engineer | Donchian, NR4/NR7, vol-contraction breakouts. |

### 🔧 Optimization
| File | Role | What it does each cycle |
|---|---|---|
| [06-strategy-optimizer.md](06-strategy-optimizer.md) | Strategy Optimizer | Searches Trader Dev, forks winners, improves one variable. |
| [07-position-optimizer.md](07-position-optimizer.md) | Position Optimizer | Tunes leverage, Kelly, vol-targeting, drawdown throttle. Keeps entries frozen. |

### 🛡 Risk & robustness
| File | Role | What it does each cycle |
|---|---|---|
| [08-risk-manager.md](08-risk-manager.md) | Risk Manager | Audits the desk, rejects fragile/overfit/reckless systems. |
| [09-drawdown-auditor.md](09-drawdown-auditor.md) | Drawdown Auditor | Stress-tests drawdown, recovery time, longest losing streak. |
| [10-overfitting-detector.md](10-overfitting-detector.md) | Overfitting Detector | Walk-forward, parameter sensitivity, multi-pair stability checks. |

### 📐 Structural & pattern-based
| File | Role | What it does each cycle |
|---|---|---|
| [11-multi-timeframe-strategist.md](11-multi-timeframe-strategist.md) | Multi-Timeframe Strategist | HTF context + LTF entry; the most consistent pro upgrade. |
| [12-liquidity-sweep-hunter.md](12-liquidity-sweep-hunter.md) | Liquidity Sweep Hunter | Stop-hunt and sweep-and-reverse behaviour around price levels. |
| [14-pattern-recognition-strategist.md](14-pattern-recognition-strategist.md) | Pattern Recognition Strategist | Engulfing, pin, inside-bar, three-bar — only at structural locations. |

### 🧪 Experimental (calendar / time-based)
| File | Role | What it does each cycle |
|---|---|---|
| [13-moon-phase-strategist.md](13-moon-phase-strategist.md) | Calendar & Lunar Cycle Strategist | Pure date-math hypotheses: lunar, halving, weekly, session, expiry effects. Honest baselines. |

## How to combine roles

A real hedge fund runs many specialists at once. So can you. A practical 24/7 desk:

| Cadence | Role | Why |
|---|---|---|
| Every 15m | `00-ai-hedge-fund-manager` | Picks the next priority job |
| Every 15m | `01-quant-mathematician` | Greenfield idea pipeline |
| Every 15m | `06-strategy-optimizer` | Improves the existing book |
| Every 30m | `07-position-optimizer` | Tunes capital allocation |
| Every 1h  | `08-risk-manager` | Audits the desk for fragility |
| Every 6h  | `10-overfitting-detector` | Catches curve-fits before they go live |
| Daily     | `11-multi-timeframe-strategist` | Adds HTF discipline to the book |
| Weekly    | `13-moon-phase-strategist` | Rigour benchmark — your real edges should beat calendar baselines |

Each loop produces a structured report. Save them, compare them, promote winners through Trader Dev's strategy lifecycle (`promote_strategy` / `demote_strategy`).

## Required MCP tools

All loops use the Trader Dev MCP server. Most-used tools across the desk:

- `mcp__trader-dev__search_strategies` — discover existing strategies
- `mcp__trader-dev__create_strategy` / `update_strategy` / `fork_strategy` — version research
- `mcp__trader-dev__run_backtest` / `quick_backtest` — backtest Pine Script
- `mcp__trader-dev__optimize_strategy` — automated parameter sweeps
- `mcp__trader-dev__compare_backtests` — diff fork vs original
- `mcp__trader-dev__get_backtest_result` / `get_equity_curve` / `get_trades` — pull metrics
- `mcp__trader-dev__promote_strategy` / `demote_strategy` — lifecycle management

Always call `tools/list` first. Never guess arguments.

## Loop discipline (read this once)

1. **TradingView-native only.** Every strategy must be Pine-backtestable. No off-chain data feeds.
2. **Each fire is independent.** Do not assume context from the previous cycle exists.
3. **One productive cycle per fire.** Pick one strategy, do one job, write one report.
4. **Persist to Trader Dev, not to chat history.** Use `create_strategy` / `update_strategy` so work survives across cycles.
5. **Fail fast.** If the cycle hits a dead end (no candidates, MCP errors, weak edge), report and stop — don't pretend.
6. **Honest verdicts only.** Reject / Watchlist / Incubate / Candidate / Production candidate. No hype.
7. **No live trading from a loop.** Loops are research and backtesting only. Live execution always requires human review.

## Risk notice

This is a research desk, not a trading bot. Loops generate hypotheses and backtests. They do not place real orders. Crypto is risky, leverage is risky, backtests are not future performance. See [docs/DISCLAIMER.md](../docs/DISCLAIMER.md).
