# Agent Guide

This repo is designed to be read by AI agents.

## Before doing anything

1. Read `SKILL.md`.
2. Confirm Trader Dev MCP is connected.
3. Inspect available MCP tools and schemas.
4. Do not guess missing tool arguments.
5. Ask for missing information only when required.

## Research modes

### New strategy research

Use when the user wants original strategy ideas.

Rules:

- Build from first principles.
- Do not use old website strategies.
- Do not fork existing strategies.
- Start with a mathematical hypothesis.
- Backtest the new Pine Script with Trader Dev.

### Strategy optimisation

Use when the user wants existing strategies improved.

Rules:

- Start with `mcp__trader-dev__search_strategies` where available.
- Pick strategies with potential.
- Fork before editing.
- Change one main idea at a time.
- Compare every fork against the original.

### Position optimisation

Use when the user wants to improve capital allocation.

Rules:

- Do not change signal logic.
- Optimise sizing, leverage, Kelly, drawdown control, volatility targeting, and bounded recovery logic.
- Always report liquidation and risk-of-ruin concerns.

## Result discipline

Every report should answer:

- What was tested?
- Why was it tested?
- What changed?
- Did it improve risk-adjusted performance?
- Did drawdown increase?
- Did it work across multiple symbols?
- Did it work across nearby timeframes?
- What should happen next?
