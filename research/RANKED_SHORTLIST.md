# RANKED SHORTLIST

Current top priorities (research value and prior credibility). No backtest metrics are reported.

## This cycle (fourth research cycle)

Material evidence update, one new hypothesis, one scoring correction.

1. Evidence base corrected: the published Management Science version of "Crypto Carry" (Schmeling, Schrimpf & Todorov, published online 6 May 2026) and the revised BIS working paper (October 2025) run March 2019 to July 2024, not to January 2022 as cycles 1-3 recorded. The "post-2022 validity gap" is therefore narrower than previously recorded (the published sample now covers 2022-2024), and the open window has moved to after July 2024 and to the transfer from dated futures to retail perpetual venues.
2. Strongest contrary evidence added to the two existing entries: He, Manela, Ross & von Wachter (2026) show past returns explain more than half of the futures-spot gap (momentum / positive feedback), which is a competing explanation for both the basis level and for funding extremes; Gornall, Rinaldi & Xiao (2025) show perpetuals now dominate derivatives volume and reduce extreme price dislocations; Garcia Seuma (2026) shows pre-crash signatures are event-heterogeneous, invert out of sample, and vanish for news-driven shocks.
3. CRYPTO-EDGE-003 added: cross-venue funding dispersion as a venue-specific relative-value signal, the mechanism that He et al. explicitly flag as an open research avenue and that Zhivkov (2026) documents as persistent but mostly unprofitable after costs for pure funding capture.
4. Scoring correction: the rubric formula (score / 5 x dimension weight) had been applied at half value to the two 10%-weight dimensions in cycle 1. Totals are restated; no dimension score changed except one documented robustness downgrade on CRYPTO-EDGE-002.

| Rank | ID | Thesis | Total score | Confidence | Main mechanism | Decisive advantage | Largest uncertainty | Free-data feasibility | Next research step |
|------|-----|--------|-------------|------------|----------------|--------------------|---------------------|-----------------------|--------------------|
| 1 | CRYPTO-EDGE-001 | Elevated perpetual basis (carry) predicts negative spot returns and rising sell liquidations over 1-4 weeks | 73/100 | Medium | Constrained cash-and-carry arbitrage plus trend-chasing leveraged retail demand; forced sell unwind | Peer-reviewed evidence with sample to July 2024 (Management Science 2026; BIS WP 1087 rev. Oct 2025) and a liquid, liquidatable signal | Momentum explains much of the basis, so the raw signal may be a momentum proxy; published evidence is on dated futures, not retail perps; pre-crash signatures are event-heterogeneous | Confirmed free: Binance/Bybit/OKX funding endpoints and Binance public archives; liquidation detail unverified | Test whether carry-crash persists after July 2024 and on perps, and whether momentum-residualized basis beats raw basis |
| 2 | CRYPTO-EDGE-003 | Extreme cross-venue funding dispersion predicts relative underperformance of the expensive venue over 5-20 days | 61/100 | Low-medium | Segmented cross-venue arbitrage (no cross-margining), liquidity heterogeneity, venue-specific premia | Differencing across venues removes the market-wide carry and momentum component that confounds 001 and 002; mechanism documented in primary sources | No direct evidence for the predictive mapping; sign may invert if the expensive venue leads price discovery; cost-adjusted dispersion trades mostly fail | Confirmed free for funding history at Binance/Bybit/OKX; per-venue mark price history depth unverified | Check whether the dispersion effect survives momentum/basis residualization and a cost model, or should be rejected |
| 3 | CRYPTO-EDGE-002 | Extreme funding-rate deciles predict short-horizon mean reversion opposite the funding extreme | 58/100 | Low | Crowded leverage; forced-liquidation positive feedback (Garcia Seuma 2026; BitMEX 2021) | Fully free inputs; contrarian direction can align with funding receipt | Thin published evidence; funding is proportional to the futures-spot gap, so the signal may be momentum reversal in disguise; extremes are rare (IQR 1.20 bps CEX) and rarer in the perp era | Confirmed free for funding and price | Assess incremental power over basis and momentum, and whether the tail mass supports a preregistered decile test |

Scoring rubric (weighted): causal mechanism 20%, evidence 15%, robustness 15%, free-data access 15%, net value after frictions 15%, falsifiability 10%, originality 10%. Contribution per dimension = (score / 5) x weight, summing to 100. Scores are research priority, not profit probabilities.

## New this cycle
- CRYPTO-EDGE-003 (Cross-Venue Funding Dispersion) added at rank 2, 61/100, confidence low-medium. Mechanism documented in He et al. (2026) and Zhivkov (2026); predictive mapping is a new, explicitly falsifiable claim with a symmetric design (reversed-sign placebo, liquidity filtering, momentum/basis residualization).

## Downgraded/rejected
- CRYPTO-EDGE-002 robustness lowered 3/5 -> 2/5 and confidence lowered low-medium -> low on new contrary evidence (perp-era dislocation compression, funding clustering near zero, momentum confounding). Total moves from a corrected 61 to 58; rank 2 -> 3.
- No hypothesis rejected this cycle. Recorded in REJECTED_AND_DEFERRED.md: the pure cross-venue funding-capture variant (not viable after costs per Zhivkov 2026) is rejected as a return source and folded into CRYPTO-EDGE-003 as a directional relative-value claim; a crypto options IV-slope return predictor is rejected because published evidence finds IV slopes forecast volatility but lack return predictive capability; the spot-ETF-flow candidate is deferred with a specific reason (flow endogeneity).

## Statement
No empirical strategy validation (backtests, paper trading, forward tests, parameter sweeps) was performed in this repository. This is research documentation only.
