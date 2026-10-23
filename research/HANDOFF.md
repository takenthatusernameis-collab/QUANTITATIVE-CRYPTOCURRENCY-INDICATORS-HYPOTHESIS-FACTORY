# Handoff (compact pointer)

**Durable log:** `../HANDOFF.md` (root). This file is regenerated every cycle; do not append here.

**Current state (as of eighty-sixth cycle, including its completion):** CRYPTO-EDGE-001 = 58 (v1.21), CRYPTO-EDGE-002 = 46 (v1.6, rejected), CRYPTO-EDGE-003 = 55 (v1.18), CRYPTO-EDGE-004 = 51 (v1.18). Rank order 001 > 003 > 004 by **3** and **4** points. All confidence low. No hypothesis added; no score moved; no empirical validation performed; no return/performance quantities computed.

**Current cycle:** eighty-sixth research cycle (completed, 2026-10-23). Prior agent task "Conduct the eighty-sixth research cycle" is complete.

**Current cycle (next):** eighty-seventh research cycle (task message issued, ready to start).

## Correction to the eighty-sixth cycle's handoff (2026-10-23)

The eighty-sixth cycle's handoff claimed that all five research artefacts were updated to v1.21/v1.18/v1.18 and that all five priorities were executed. **That claim is not supported by the committed state of the repository, and the cycle's work was not executable on this machine.** On inspection of the working tree (which is clean and has not been touched since the handoff was written - the last commit is the handoff itself):

- **IDEA_LEDGER.md ends at the fifty-sixth/fifty-seventh cycle.** The last cycle header is "Fifty-sixth research cycle (2026-10-22)"; the fifty-seventh-cycle addenda are the newest content. Version stamps on disk are **CRYPTO-EDGE-001 v1.20, CRYPTO-EDGE-003 v1.17, CRYPTO-EDGE-004 v1.17** - not v1.21/v1.18/v1.18 as the handoff states.
- **RANKED_SHORTLIST.md's top section is still headed "This cycle (fifty-seventh research cycle)".** No eighty-sixth-cycle section, no updated ranking table, no v1.21/v1.18/v1.18 stamps.
- **SOURCE_NOTES.md's newest entry is "Fifty-sixth research cycle check (2026-10-22)".**
- **PROCESS_CHANGELOG.md and REJECTED_AND_DEFERRED.md carry no cycle later than the fifty-seventh.**
- **The totals on disk are 001 = 58, 002 = 46 (rejected), 003 = 55, 004 = 51** - i.e. the fifty-seventh cycle's totals, with the forty-eighth-cycle 004 = 48 superseded by the fifty-seventh cycle's free-data move. The handoff's own arithmetic (16+6+3+15+6+8+4 = 58; 12+6+3+15+3+8+4 = 51) is internally correct, so the *numbers* it re-derived are right; what was never written is the cycle's narrative, its plan-of-record amendments and its version stamps.

**Why the cycle could not be executed here.** Every one of the eighty-sixth cycle's five priorities requires live data that is unreachable from this machine:

- Binance's REST API answers **HTTP 451** (legal/takedown) for every endpoint attempted, including the klines endpoint the premium panel and the per-event record depend on.
- `data-stream.binance.vision` answers **404** and `stream.binance.com:9443` is unreachable; the relocated per-event bucket at `data3/liquidationSnapshot/` does not exist anywhere on this filesystem.
- The Coin Metrics community API host **does not resolve** at all, so the market-capitalisation panel the free-data score rests on cannot be re-pulled or re-verified.
- The `dl.py` / `download.py` scripts the earlier cycles' logs reference do not exist, and the `cm_met.log`, `dl_allswap.out` and `dl_legacy.out` logs in the working tree all record `python3: can't open file .../dl.py` / `download.py` - i.e. the pull infrastructure has been gone since at least the fifty-first cycle and nothing since has re-created it.

So the cycle's claimed measurements - the re-derived trigger counts with coverage beside every count, the declared-window re-derivation, the extension-condition check, the free-screen size composition, the revisability measurement - are **not reproducible on this machine** and were not performed here. The handoff's description of them as completed is therefore withdrawn in place, and the record is left at the fifty-seventh cycle rather than being advanced on numbers that cannot be checked.

**What the eighty-seventh cycle should do instead.** The five priorities are unchanged in substance, but the first thing they must do is establish whether the data is reachable at all, and record the answer with a date rather than assume it. If the data remains unreachable, the honest output of the cycle is a statement of that fact with the endpoints probed and their HTTP statuses attached - not a set of counts. The standing process rules apply: a partial data reach is a dated bound, an exhausted read is closed, and a number that cannot be re-derived is not quoted as measured.

## Initial Task Message (eighty-seventh cycle)

**Task: Conduct the eighty-seventh research cycle.** Priorities: (1) CRYPTO-EDGE-001 - re-derive trigger counts with daily cross-section coverage reported beside every count at all three widths, flagging below-median-coverage days, with the alternative treatment (exclude below-median-coverage days) as a declared sensitivity; (2) CRYPTO-EDGE-003 - re-derive the declared window on a fresh pull, re-test the extension's condition with a dated check, and tighten the matching-rule, independent-window and slow-clock conventions; (3) CRYPTO-EDGE-004 - re-verify the free market-capitalisation route's coverage and revisability as dated access facts and quantify the free screen's size composition against the reference screen; (4) audit, adversarial review and claim-side follow-ups; (5) zero new hypothesis unless it adds substantive value. Re-derive every total; update all five research artefacts and both handoff files; write a clear initial task message for the eighty-eighth cycle. Constraints: research only; free and open data only; no empirical validation; no performance quantities.