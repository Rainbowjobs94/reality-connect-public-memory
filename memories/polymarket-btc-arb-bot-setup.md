# Polymarket BTC Yes+No Arbitrage Bot Setup (Public Memory)

**Updated**: 2026-10-18
**Purpose**: Safety-first, paper-first trading agent design for Reality Connect / Miracle Network / IA Guardian knowledge building. Intended to generate transferable lessons and optional micro-value toward higher-tier AI access. No guarantees of profit.

## Core Strategy (from public guide)
Binary markets pay $1 or $0 at resolution. Owning one Yes + one No is a guaranteed $1. When Yes ask + No ask < 1.00 by a minimum edge (start ≥ 0.02 after fees), buy both legs or neither. Never hold a naked side. Merge the pair immediately to recycle capital. Focus on liquid BTC Up/Down markets.

## Improved Reality Connect Integration
- Default mode: pure paper / dry-run. Log every gap, would-be action, both-legs logic, merge simulation, and outcome.
- Hard rules: min edge after fees, both-or-neither, immediate unwind on partial fill, daily/overall loss kill switch, tiny sizing only if live is later authorized.
- Structured logging for knowledge transfer to Miracle Network agent layer / IA Guardians (markdown summaries of lessons).
- Hybrid optional: light Coinbase monitoring (existing ~$13 USDC + POL) for order-flow tests only with explicit approval. Primary engine remains Polymarket BTC arb paper.
- Role split: watcher agent (price stream + edge detect) + executor (both legs / unwind / merge). User owns strategy; agent handles plumbing (Grok Build / Grok Bot).

## Recommended Bot Role Prompt
```
You are the Reality Connect Trading & Arb Agent.

Primary strategy (paper by default):
- Monitor liquid BTC Up/Down binary markets on Polymarket.
- Detect when Yes ask + No ask < 1.00 by a minimum edge (start at 0.02 after fees).
- If gap found: attempt both legs or neither. Never hold a naked side. Immediately unwind any one-legged fill.
- After both fill: merge the pair back to collateral ASAP to recycle capital.
- Log every decision, calculation, fill status, merge, and outcome in structured format for knowledge transfer to the Miracle Network agent layer.

Hard rules:
- Default = paper only. No real orders until dry-run validation and explicit tiny-size approval.
- Kill switch: stop on preset loss limit or anomalies.
- Always use ask prices for gap detection. Prefer resting/maker orders where practical.
- Produce periodic Knowledge Transfer Summaries.
- Capital preservation and clear, verifiable logic over returns.

Start in pure dry-run/paper on one BTC market. Report gaps found, what you would have done, and any lessons.
```

## Polymarket Funding via Coinbase (user-executed)
1. On Polymarket: Deposit → Transfer Crypto → USDC → Polygon → copy deposit address.
2. On Coinbase: Send USDC on the exact Polygon network to that address. Start with a tiny test amount.
3. Confirm on Polymarket. Always match network (Polygon) to avoid loss.
Note: Coinbase tools available here support balances/orders but not direct unattended withdrawals. User must initiate any send.

## Next Recommendations (paper-first)
- Create the Bot in Grok Bot / Grok Build with the role above.
- Run dry-run for days; review logs.
- Only then consider tiny real capital you can afford to lose entirely.
- Combine with non-trading savings (bill negotiation etc.) for more reliable contribution toward Ultra / higher tiers.
- Continue pushing structured lessons into this public memory repo for agent continuity.

**Safety**: Crypto and prediction-market trading can lose capital. This is educational / research scaffolding only. Verify eligibility, fees, and all details yourself. Public results claimed by others are not guarantees.

Related files: grok-bot-routines.md, development-status-public.md
