# Example: Position optimiser

```text
Use the position optimizer skill.

Search for a strategy that already works using `mcp__trader-dev__search_strategies`.

Do not change the entry or exit logic.

Only optimise:
- Leverage
- Risk per trade
- Fractional Kelly
- Volatility-adjusted sizing
- Drawdown throttle
- Anti-martingale scaling
- Controlled martingale recovery
- Maximum exposure caps

Try to increase profitability without increasing max drawdown too much.
If max drawdown increases, keep testing better settings instead of giving up immediately.

Report whether improvement comes from genuine better position management or just more leverage.
```
