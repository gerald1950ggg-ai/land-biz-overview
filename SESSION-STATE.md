# SESSION-STATE.md - Current Working Memory

## Current Project: Qullamaggie Autoresearch Loop (Trading Algorithm)

**Status**: RESUMING — previous session interrupted at iter16

**Current Best**: iter15 (PF=4.002)
- Extension filter: 1.50x → 2.00x SMA50
- VCP: 0.92 (95% of 20-day range contraction)
- 72 trades, 36.1% win rate, 94.2% net profit

**Last Action**: Killed hanging iter16 backtest (extension filter 3.00x was too loose)

## Key Findings This Session
1. **iter15 was the breakthrough**: Extension filter relaxation from 1.50x to 2.00x improved PF from 3.96 to 4.002
2. **Score weighting is neutral**: Tried contraction 3x→5x, momentum 10x→6x, MIN_SCORE 17→15 (iter14) → got same PF=3.766 as iter7
3. **VCP axis exhausted**: Tried 0.85, 0.89, 0.91, 0.92 — 0.92 is optimal
4. **Extension filter has limits**: 1.50→2.00 ✅ good, 2.00→3.00 ✗ too much (hung)

## Next Steps (when QC budget available)
- [ ] Try extension filter 2.25x (between 2.00 working and 3.00 broken) 
- [ ] Try MIN_SCORE=16 with extension 2.00x (more trades, possibly better PF)
- [ ] Consider VCP=0.90 (slight tighten) to optimize candidates
- [ ] Explore other axes: watchlist_threshold, ADR_MIN, RS_PERCENTILE

## QC Compute Status
- ~830 minutes used (monthly budget likely ~1000)
- Free plan with B2-8 node
- 16 backtests run this session
- Still have compute capacity for 2-3 more iterations

## Code State
- Branch: autoresearch/mar26
- HEAD: b93210d (session summary)
- Working tree clean
- Main file: qc-cloud/main.py (currently at iter15 state, ready for next test)

---

**Important**: Previous agent session was aborted. This session resumed at 2026-03-27 08:44 MST (14:44 UTC).
