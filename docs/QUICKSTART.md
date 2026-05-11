# Quick Start

## 1. Install Trader Dev MCP

### Claude Code

```bash
claude mcp add --transport sse --scope user trader-dev https://mcp.trader.dev/sse
```

### Codex

```bash
codex mcp add trader-dev -- npx -y mcp-remote https://mcp.trader.dev/sse
```

### OpenClaw

Add this SSE MCP endpoint:

```text
https://mcp.trader.dev/sse
```

## 2. Give your agent this message

```text
Read https://raw.githubusercontent.com/DaviddTech/ai-trading-agent/main/SKILL.md and confirm Trader Dev MCP is connected.
```

## 3. Run your first backtest

```text
I am going to paste a Pine Script strategy.
Backtest it with Trader Dev on crypto pairs.
Report the baseline first. Do not optimise until we understand the strategy.
```

## 4. Choose a research mode

- New strategy: use `skills/quant-mathematician/SKILL.md`
- Mean reversion: use `skills/mean-reversion-engineer/SKILL.md`
- Existing strategy improvement: use `skills/strategy-optimizer/SKILL.md`
- Position sizing: use `skills/position-optimizer/SKILL.md`

## 5. Read the report

Look for:

- Robustness across symbols
- Robustness across timeframes
- Max drawdown
- Profit factor
- Average trade
- Number of trades
- Whether one outlier trade explains the result

Do not trust one good backtest.
