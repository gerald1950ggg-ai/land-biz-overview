# SESSION-STATE.md — Active Working Memory

*This file is Gerald's "RAM" — survives compaction, restarts, distractions.*

## Current Task  
Karpathy autoresearch loop: Autonomous trading algorithm iteration (Qullamaggie breakout strategy on QuantConnect)

## Key Context  
- Project: `/projects/trading/quantconnect/` (QC project 28157266, user 404912)
- Strategy: Qullamaggie-style breakout trades, swing holding (6 days avg)
- Backtest: 2023-01-01 to 2024-06-30 (in-sample), 2024-07-01 to 2025-12-31 (holdout)
- Baseline COMPLETE: PF 1.479, 236 trades, WR 29.7%, DD 78.2%
- Loop architecture: Modify → Compile → Backtest → Orders → Evaluate → Charts → Log → Iterate

## Hard Guidelines (Coose-approved scope)
- BREAKOUT TRADES ONLY (no parabolic shorts, no EP/earnings plays — those come later)
- 90-day (3-month) setup window ahead of entry
- Trading environment filter: QQQ 10/20/50 SMA alignment (good environment only)
- Philosophy: Dial in ONE strategy in ONE environment perfectly, then expand
- Do NOT use Qullamaggie avatar skill (not ready)
- Chart checkpoint at each "keep" iteration — 90 days before + 60 days after each trade to diagnose early/late entries AND exits
- We CANNOT predict tops — don't optimize for hindsight exit timing

## Architecture: Karpathy Autoresearch Loop
- ONE agent with a great program.md (not multi-agent debate)
- program.md combines: Qullamaggie methodology + QC technical reference + evaluation framework
- Loop: modify algo → git commit → run backtest → evaluate → keep/discard → repeat
- Chart visual checkpoint after every "keep" decision (5 worst + 3 best trades)
- Charts must show enough timeframe to diagnose BOTH early/late entry AND early/late exit
- In-sample only (2023-mid 2024). Out-of-sample (mid 2024-2025) checked periodically.
- Future: expand single agent into multi-agent team when loop plateaus

## Completed Tasks (Full Phase)
- ✅ QC credentials, projects verified
- ✅ Qullamaggie knowledge base: 16 files, ~170KB (breakout-setups/, general/, raw transcripts)
- ✅ Knowledge docs: evaluation-framework.md, qc-technical-reference.md, program.md (12.5KB)
- ✅ Loop infrastructure: runner.py (25KB), compile/backtest/orders/evaluate/charts pipeline
- ✅ Git initialized (autoresearch/mar26 branch)
- ✅ DECISION-LOG.md created (10 decisions + 3 corrections)
- ✅ **BASELINE BACKTEST COMPLETE** (2026-03-26 18:54 UTC)
  - Backtest ID: 3fd3398295ccdd6ff9e0df1f33c70410
  - Profit Factor: 1.479
  - Trades: 236
  - Win Rate: 29.7%
  - Max Drawdown: 78.2%
  - Charts: autoresearch/charts/iter_001_baseline/
  - Guardrails calibrated to baseline reality

## In Progress
- None — baseline complete, loop ready for first iteration

## Next Actions (Coose's direction)
1. Review baseline charts (5 worst + 3 best) — diagnose entry/exit timing
2. Run first autonomous iteration (likely: extension filter or dynamic watchlist size)
3. Extract ground truth trades from Qullamaggie transcripts (for comparison charts)
4. Research QC resolution optimization (daily screening + 5-min entries)

## Documentation Requirements (Coose priority)
- Document everything so this becomes a REUSABLE PATTERN for future trading agents
- Goal: "trading agent creator agent" / "autoresearcher agent" template
- Every decision, every iteration, every lesson learned gets captured
- This project should teach future-us how to build the NEXT trading autoresearch project faster

## Discussion Notes (2026-03-26 18:12)
- Coose suggests: Focus backtest on timeframe where QQQ is "market on" — skip dead periods
- Shorten to 9-12 months to reduce backtest time
- Since runs take ~40min, invest MORE in analysis between runs (quality over quantity)
- More charts per iteration (10+) 
- KEY INSIGHT: Cross-reference our trades against Qullamaggie's known trades from same period
  - His transcripts mention specific tickers and dates
  - We can compare: did we catch what he caught? Did we take trades he wouldn't?
  - Charts should include HIS setups that we MISSED (false negatives), not just our trades
- This is a DISCUSSION — no changes made yet, revisit after baseline completes

## Discussion Notes (2026-03-26 18:18)
- QC Resolution question: Do we need minute-by-minute? 
  - Current algo uses 30-min OR with 5-min consolidator for breakout detection
  - Qullamaggie uses 1-min, 5-min, and 60-min (=30min for opening) OR timeframes
  - If we only care about 30-min OR breakouts, could we use 5-min resolution instead of 1-min? Major speed boost.
  - NEED TO VERIFY: Does QC allow mixed resolution? Can we use daily for screening + 5-min for entry?
- Dynamic OR timeframe: Could adapt which OR timeframe (1/5/30 min) based on signals
  - Volatile days → shorter OR (1-min)
  - Quiet days → longer OR (30-min)
  - This is FUTURE — get basic loop working first
- Dynamic position sizing based on real-time signals — also future
- Coose is thinking out loud — capture ideas, don't act on them yet

## TODO: Post-Discussion Tasks (do after current conversation)
1. Extract ticker/date pairs from Qullamaggie transcripts (his known great setups)
2. Build ground truth comparison into chart checkpoint (our trades vs his calls)
3. Research optimal QC resolution for this strategy (minute vs 5-min vs mixed)
4. Identify "market on" periods in 2023-2024 for focused backtest window
5. Update program.md and runner.py with refined approach after baseline results

## Knowledge Base Location
`/Users/gerald/.openclaw/workspace/projects/trading/quantconnect/knowledge/`
- evaluation-framework.md ✅
- qc-technical-reference.md ✅
- breakout-setups/ ⏳ (subagent building)
- parabolic-shorts/ ⏳ (subagent building)
- episodic-pivots/ ⏳ (subagent building)
- intraday/ ⏳ (subagent building)
- general/ ⏳ (subagent building)
- raw_transcripts/ ✅ (17 new transcripts)

## WAL Protocol Notes
- Write to this file BEFORE responding to user, not after
- Triggers: User preferences, decisions, deadlines, corrections
- Purpose: Ensure context survives crashes/compaction

---
*Last updated: 2026-03-26 18:55 MDT (baseline complete)*
*WAL Protocol: ACTIVE*
