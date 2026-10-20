# Durable Handoff

## Prior Task
The prior agent task was: "Read the prior agent task from the durable handoff and complete it. Then update the handoff and write a clear initial task message for the next agent."

## Status
Completed (first research cycle).

## Work Done
- Re-read SYSTEMATIC_CRYPTO_EDGE_HYPOTHESIS_RESEARCH_PROMPT.txt and research artefacts.
- Scanned public literature for candidate mechanisms (funding rates, open interest, liquidations, perpetual basis/carry). Sources documented in research/SOURCE_NOTES.md with access classification:
  - BIS WP 1087 "Crypto carry" (confirmed free PDF) — high carry predicts crashes/sell liquidations.
  - Chi (2023) J. Futures Markets doi:10.1002/fut.22425 (abstract only) — basis strongest cross-sectional crypto futures factor.
  - Garcia Seuma (2026) arXiv:2607.27070 / 2608.03616 (confirmed free) — liquidation cascade mechanics.
  - arXiv:2102.04591 (confirmed free) — BitMEX forced liquidations, ~60X avg leverage among liquidated.
  - NBER w24877 (confirmed free) — context only.
- Developed 2 candidate hypotheses with full standardized records (prompt sections 1-17), added to research/IDEA_LEDGER.md:
  - CRYPTO-EDGE-001 Basis/Carry Reversal v1.0 — 67/100, medium confidence.
  - CRYPTO-EDGE-002 Funding Extreme Contrarian v1.0 — 53/100, low-medium confidence.
- Ranked candidates in research/RANKED_SHORTLIST.md with scoring rationale.
- Recorded process change in research/PROCESS_CHANGELOG.md.
- All work strictly research-only (no backtests, no implementation, no validation execution).

## Next Task — initial message for the next agent

You are the research-theory agent for this quantitative cryptocurrency indicators hypothesis factory. Your mission and scope are defined in SYSTEMATIC_CRYPTO_EDGE_HYPOTHESIS_RESEARCH_PROMPT.txt (research only: no backtests, no implementation, no empirical validation, no paid data, no workflow/infrastructure changes).

Conduct the second research cycle, following the continuous iteration loop in the prompt:

1. Re-read the research prompt and current artefacts (research/IDEA_LEDGER.md, research/RANKED_SHORTLIST.md, research/SOURCE_NOTES.md, research/PROCESS_CHANGELOG.md, research/REJECTED_AND_DEFERRED.md).
2. Audit the current ranked shortlist: CRYPTO-EDGE-001 (rank 1, 67/100) and CRYPTO-EDGE-002 (rank 2, 53/100). Check duplication, weak causal links, missing contrary evidence, free-data feasibility, ranking consistency, and unsupported confidence.
3. Pursue the highest-value open question: whether funding-rate extremes (CRYPTO-EDGE-002) add incremental predictability beyond the basis/carry measure (CRYPTO-EDGE-001), and whether the carry-crash relation holds post-2022 across current perpetual venues. Search public, freely accessible literature/documentation as needed.
4. Add 0-1 new hypotheses only if they add substantive value — there is no quota; do not invent weak ideas.
5. Adversarially challenge each candidate: what would have to be true? What is the most likely alternative explanation? Why might the opportunity already be priced in? What would falsify it?
6. Re-score and re-rank the shortlist using the standard rubric; update IDEA_LEDGER.md and RANKED_SHORTLIST.md.
7. Record changes, citations, sources checked, and reasons ideas moved up/down/stayed/were rejected; update PROCESS_CHANGELOG.md if the process itself is improved (never by allowing backtests, implementation, paid dependencies, or scope drift).
8. End the cycle with a report: substantive research completed; changes to the shortlist and why; independent sources/contrary arguments reviewed; remaining uncertainties and the highest-value next question; a clear statement that no empirical validation was performed; any blocker to free data or falsifiability.

Deliverable: updated research artefacts plus an updated HANDOFF.md with this cycle marked complete and a new initial task message for the following agent.

## Notes
No empirical strategy validation performed. All changes are research-documentation only.
