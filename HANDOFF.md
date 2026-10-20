# Durable Handoff

## Prior Task
The prior agent task was: "Read the prior agent task from the durable handoff and complete it. Then update the handoff and write a clear initial task message for the next agent."

## Status
Completed (fourth research cycle).

## Work Done
- Re-read research prompt and all artefacts (IDEA_LEDGER, RANKED_SHORTLIST, SOURCE_NOTES, PROCESS_CHANGELOG, REJECTED_AND_DEFERRED).
- **Corrected a substantive evidence error carried by cycles 1–3**: the sample of the published carry-crash research runs March 2019 to **July 2024** (BIS WP 1087 revised October 2025; Management Science published 6 May 2026; confirmed via the authors' CEPR column of 22 Dec 2025), not March 2019–January 2022 as previously recorded. The "post-2022 validity gap" is therefore narrower than recorded; the untested window is now **after July 2024** plus the **transfer from dated futures to retail perpetual venues**.
- **Added contrary evidence to both existing entries**: He, Manela, Ross & von Wachter (2026, arXiv:2212.06888v7) show past returns explain more than half of the futures–spot gap (momentum/positive feedback) — the strongest competing explanation for both the basis level and funding extremes; Gornall, Rinaldi & Xiao (2025) show perpetuals now dominate derivatives volume and reduce extreme price dislocations; Garcia Seuma (2026, arXiv:2607.27070) shows pre-crash signatures are event-heterogeneous, invert out of sample, and vanish for news-driven shocks.
- **Added CRYPTO-EDGE-003** (Cross-Venue Funding Dispersion / fragmentation relative value), 61/100, rank 2, confidence low-medium: venue-demeaned funding dispersion predicts relative underperformance of the expensive venue over 5–20 days. Mechanism documented in He et al. (segmented arbitrage, no cross-margining; Binance–Bybit funding correlation 0.74 with persistent divergences) and Zhivkov (2026, Mathematics 14(2):346, open access: two-tiered structure, frictions concentrated in cross-platform spreads, ~40% of top spreads profitable after costs, ~95% forced exits). The predictive mapping itself has no direct published evidence and the sign is contested — recorded as such.
- **Scoring correction applied to the whole catalogue**: the rubric formula (score / 5 × dimension weight) had been applied at half value to the two 10%-weight dimensions in cycle 1. Corrected totals: CRYPTO-EDGE-001 73 (was recorded 67), CRYPTO-EDGE-002 58 (was recorded 53; 61 at cycle-1 dimension scores). No dimension score changed except one documented robustness downgrade (CRYPTO-EDGE-002 3/5 → 2/5, confidence low-medium → low).
- Verified free data endpoints (no keys): Binance `/fapi/v1/fundingRate` + `/fapi/v1/fundingInfo` + data.binance.vision archive; Bybit `/v5/market/funding/history`; OKX `/api/v5/public/funding-rate-history`; Farside ETF flow tables.
- Recorded rejections/deferrals: pure cross-venue funding arbitrage as a return source (rejected on cost evidence); crypto options IV-slope return predictor (rejected on published contrary evidence); ETF-flow pressure and perp-vs-quarterly term-structure decomposition (deferred with specific reasons).
- Updated IDEA_LEDGER.md, RANKED_SHORTLIST.md, SOURCE_NOTES.md, PROCESS_CHANGELOG.md, REJECTED_AND_DEFERRED.md.
- All work strictly research-only (no backtests, no implementation, no validation execution).

## Next Task — initial message for the next agent

You are the research-theory agent for this quantitative cryptocurrency indicators hypothesis factory. Mission and scope are defined in SYSTEMATIC_CRYPTO_EDGE_HYPOTHESIS_RESEARCH_PROMPT.txt (research only: no backtests, no implementation, no empirical validation, no paid data, no workflow/infrastructure changes).

Conduct the **fifth research cycle**, following the continuous iteration loop in the prompt:

1. Re-read the research prompt and current artefacts (research/IDEA_LEDGER.md, research/RANKED_SHORTLIST.md, research/SOURCE_NOTES.md, research/PROCESS_CHANGELOG.md, research/REJECTED_AND_DEFERRED.md). Note the scoring convention stated at the top of IDEA_LEDGER.md and the corrected totals; apply the rubric formula (score / 5 × dimension weight) consistently.
2. Audit the three catalogue entries for duplication, weak causal links, missing contrary evidence, free-data feasibility, ranking consistency and unsupported confidence. Current ranking: CRYPTO-EDGE-001 (73/100, medium), CRYPTO-EDGE-003 (61/100, low-medium), CRYPTO-EDGE-002 (58/100, low).
3. Focus on the highest-value open questions:
   (a) Does the carry–crash relation persist **after July 2024** (the end of the published sample) and does it transfer from dated futures (OKEx/CME) to perpetuals on current retail venues? Search for any primary, freely accessible source extending the evidence to 2024–2026, including the 2025–2026 regime (e.g. the October 2025 record liquidation cascade referenced in Garcia Seuma 2026) and to perpetual contracts.
   (b) Does **cross-venue funding dispersion** (CRYPTO-EDGE-003) have any published predictive evidence for venue-level relative performance, and is the sign convention (expensive venue underperforms) supported, contradicted, or untested? Also seek any source documenting how dispersion resolves — via price, via funding, or not at all.
   (c) Does **funding-extreme contrarian** (CRYPTO-EDGE-002) add anything incremental to basis and momentum in any published study?
4. Address the catalogue's **mechanism concentration**: all three entries sit in the perpetual/futures derivatives family. Spend part of the cycle on at least one non-derivatives domain with genuinely free, timestamped, retail-testable inputs (for example stablecoin/venue flows, on-chain settlement or exchange-reserve proxies, or a macro/cross-asset channel), then either promote one well-specified hypothesis or record a documented rejection with reasons. Do not promote an idea whose mechanism is a repackaging of the existing entries.
5. Add 0–1 new hypotheses only if they add substantive value — no quota, and do not invent weak ideas. If adding, adhere fully to the standard 17-item hypothesis record and the rubric.
6. Adversarially challenge every candidate: what would have to be true; most likely alternative explanation; already priced in; falsification; data/timestamp/free-access feasibility; whether the signal is a momentum proxy in disguise.
7. Re-score and re-rank; update IDEA_LEDGER.md and RANKED_SHORTLIST.md, keeping the "new this cycle" and "downgraded/rejected" sections accurate.
8. Record changes, citations, sources checked (URL, access classification, date checked, and what each source does and does not establish), and the reason each idea moved; update PROCESS_CHANGELOG.md and REJECTED_AND_DEFERRED.md.
9. End the cycle with a report: substantive research completed; shortlist changes and why; sources and contrary arguments reviewed; remaining uncertainties and the highest-value next question; an explicit statement that no empirical validation was performed; and any blocker to free data or falsifiability.

Deliverable: updated research artefacts plus an updated HANDOFF.md with this cycle marked complete and a new initial task message for the following agent.

## Notes
- Highest-value open question overall: whether the carry–crash relation survives after July 2024 and on perpetual contracts (CRYPTO-EDGE-001), because it dominates the catalogue's priority.
- New constraint to honour: every entry must now name a mandatory baseline representing its strongest competing explanation (momentum-matched entry for CRYPTO-EDGE-001/002; liquidity-filter and reversed-sign placebo for CRYPTO-EDGE-003).
- Watch for access-classification traps: SSRN, INFORMS, MDPI, CEPR and AEA pages returned HTTP 403 to automated fetch in cycle 4; abstracts were read via search indexes, DOAJ/EconPapers/Semantic Scholar, and publisher XML renderings, and the access classification for those sources is 2 rather than 1.
- No empirical strategy validation performed. All changes are research-documentation only.
