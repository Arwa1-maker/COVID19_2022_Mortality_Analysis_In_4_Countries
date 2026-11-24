# Covid19-deaths-africa-2022-analysis
https://github.com/owid/covid-19-data/blob/master/public/data/cases_deaths/total_deaths_per_million.csv 
### Data Quality & Cleaning Notes (2022)
- **Scope:** Filtered `total_deaths_per_million` across 2022 (365 daily records) for **Sudan**, **Egypt**, **Kenya**, and **South Africa**.
- **Completeness (`Blanks`):** Checked all four country columns and confirmed **zero missing/blank values** across the 365-day window.
- **Monotonicity Check (`Diff < 0`):** Computed day-over-day differences (`Current Day - Previous Day`) and filtered for values less than `0`; confirmed **zero negative values**, indicating no unexpected drops in the cumulative metric.
- **Reporting Cadence & Flat Periods (`Diff = 0`):** Observed multi-day stretches where daily differences equal `0` followed by discrete jumps/updates, reflecting a step-like ("staircase") reporting cadence rather than uniform day-by-day updates.
- **Retention & Aggregation Decision:** Retained all 365 daily records without dropping or altering flat periods to preserve authentic reporting patterns. When summarizing cumulative per-million values across time or months, used `Average` (instead of `Sum`) to prevent inflating cumulative figures.
