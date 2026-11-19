# CRYPTO-EDGE-001 Open-Interest-Clearing Panel — Acquisition Plan

## Symbol set
BTCUSDT, ETHUSDT (entry's specified instruments per IDEA_LEDGER.md item 4: "BTC and ETH USDT-margined perpetuals"), plus family-analogue symbols SOLUSDT, DOGEUSDT, LINKUSDT, ADAUSDT, BNBUSDT, XRPUSDT — all eight computed in cycle 922.

## Object keys (all under https://data.binance.vision)

1. **Metrics (5-min open interest):**
   `data/futures/um/daily/metrics/{SYM}/{SYM}-metrics-YYYY-MM-DD.zip`
   → CSV: `create_time,symbol,sum_open_interest,sum_open_interest_value,count_toptrader_long_short_ratio,sum_toptrader_long_short_ratio,count_long_short_ratio,sum_taker_long_short_vol_ratio`
   → 288 rows/day (00:00–23:55, 5-min cadence); earliest 2020-09-01

2. **PremiumIndexKlines (daily basis proxy):**
   `data/futures/um/daily/premiumIndexKlines/{SYM}/1d/{SYM}-1d-YYYY-MM-DD.zip`
   → CSV: `open_time,open,high,low,close,volume,close_time,quote_volume,count,taker_buy_volume,taker_buy_quote_volume,ignore`
   → `close` = premium index close (basis proxy); 1 row/day; earliest 2019-12-24

3. **FundingRate (monthly, 8-hourly):**
   `data/futures/um/monthly/fundingRate/{SYM}/{SYM}-fundingRate-YYYY-MM.zip`
   → CSV: `calc_time,funding_interval_hours,last_funding_rate`
   → ~94 rows/month; continuous

## Window
2020-09-01 → 2026-11-17 (archive lags one day; metrics tree starts 2020-09-01).

## Join / alignment rule
All three trees join on `(symbol, date)`:
- **Metrics**: `sum_open_interest` from first 5-min bar (00:00:00) = opening OI; from last bar (23:55:00) = closing OI. Clearing % = (opening − closing) / opening.
- **PremiumIndexKlines**: `close` = daily premium index close (basis). Annualized basis = close × 365.
- **FundingRate**: daily mean of `last_funding_rate` over settlements on that date (cross-check only, not used in counts).

## State definitions (pre-registered, not data-dependent)

- **Trigger state**: annualized basis > +20% (premium index close × 365 > 0.20), per IDEA_LEDGER.md item 6(P1) theory-derived starting value +20%.
- **Clearing state**: daily OI clearing % > 1% ((opening − closing) / opening > 0.01), i.e. open interest drops by more than 1% from day-open to day-close.
- **Joint state**: trigger state AND clearing state on the same (symbol, date).
- **Coverage**: fraction of (symbol, date) pairs in window with non-empty metrics + premiumIndexKlines files.

## Counts (counts of states, not returns)
Per symbol per year: trigger-state days, clearing-state days, joint-state days, total calendar days with data, coverage %.

## Effective-sample bound
Independent non-overlapping windows at horizons 1w, 2w, 3w, 4w: count windows containing ≥1 trigger day, ≥1 clearing day, ≥1 joint day.

## Constraints
- stdlib only: `csv`, `zipfile`, `urllib.request`, `statistics`, `datetime`, `json`, `os`, `concurrent.futures` (no pandas)
- No returns, spreads, drawdowns, hit rates, profit factors, Sharpe ratios, forward relationships
- Do not touch per-event arm beyond restating 281-day bound ending 2024-03-31