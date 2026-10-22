# FanSignal — Audience Intelligence Product Layer

This is an **additional web product prototype** layered on top of the original Sports Fan Engagement Dashboard research, not a replacement for its Google Trends analysis.

## Run locally

Download branch `feature/fansignal-product-layer` as a ZIP, unzip, then double-click `fansignal/index.html` in Chrome or Safari. No installation is required. The prototype loads `enhancements.js` from the same folder.

## Test data upload

1. Click **Download a sample CSV to test uploading** in the website or open [sample-data.csv](sample-data.csv).
2. Click **Upload CSV** at the top; select `sample-data.csv`.
3. Select Kansas City Chiefs, San Francisco 49ers, Dallas Cowboys, Miami Dolphins, or Philadelphia Eagles.
4. Watch the chart, momentum score, suggestions, and benchmarking update.
5. For the geographic feature, click **Upload geography CSV** and select [sample-geography.csv](sample-geography.csv).
6. Click **Export Word document** to receive an editable `.doc` decision brief, which opens in Microsoft Word or can be imported into Google Docs or Pages.

The sample CSV files contain **synthetic example values, not real Google Trends measurements.**

### Search interest CSV format

```csv
date,team,interest
2025-09-01,Kansas City Chiefs,32
2025-09-08,Kansas City Chiefs,36
```

Upload dates as `YYYY-MM-DD`, with one 0–100 value per team and date. Use eight or more observations per team for the momentum calculation. Team comparisons are valid only when query/normalization settings match.

### Geography CSV format

```csv
team,state,interest
Kansas City Chiefs,MO,82
San Francisco 49ers,CA,91
```

State must be a two-letter US postal code and `interest` a number from 0 to 100. Geographic interest **cannot be inferred from national time-series data**; it requires separately collected geographic data.

## Five product capabilities

1. **Audience momentum:** shows the last relative index, comparing averages of the latest four observations and the previous four. +10 index points = rising; -10 = cooling; otherwise stable.
2. **Geographic insights:** a state-by-state *tile heatmap*; shows synthetic placeholders until a geography CSV is uploaded. Not a geographic boundary map.
3. **Event context:** displays calendar moments (season opener, holiday football, playoffs) as illustrative reference points. It does not algorithmically identify causal drivers.
4. **Campaign opportunity engine:** translates momentum into a suggested marketing experiment and validation checks. Rule-based, not predictive.
5. **Competitor benchmarking:** ranks up to ten team search terms from the loaded data by their latest interest index. Rankings need common comparison normalization.

## What is real and what isn't

The original repo's Google Trends research is preserved. The expanded standalone web app currently uses **illustrative, generated team values**, not live Google Trends or verified actual historic results. No geographic data, event-causation evidence, site engagement, sales, ROI, or conversion rates are inferred. To make analyses real, export consistent terms/time/geography data from Google Trends and upload CSVs in the formats above.

## Structure

- `index.html`: original working single-page MVP, with expansion script loaded
- `enhancements.js`: five new features, 32-team demo coverage and Word-compatible document export
- `sample-data.csv`: ready-to-use demonstration search series
- `sample-geography.csv`: ready-to-use demonstration state interest data

## Next steps

Replace illustrative data with verified source exports; integrate documented sporting events; add a sustainable historical data pipeline, true US state geography, a campaign test planner with saved experiments, and proper cross-browser testing. Avoid claiming these are implemented already.
