# FanSignal — product layer (MVP)

**FanSignal is an additional, standalone web-app layer built on top of the original Sports Fan Engagement Dashboard research.** The original Google Trends analysis, notebook, plots, and datasets remain the analytical foundation; this new interface explores how a marketer could turn interest patterns into decisions.

## Try the prototype

Open `fansignal/index.html` in a web browser. It is a dependency-free static HTML/CSS/JavaScript application and requires no build step. You can also deploy this directory on a static host.

## Features

- Select an NFL team and compare relative search-interest time series.
- View the latest 0–100 index, four-observation momentum, and transparent rising/stable/cooling signal.
- Read **hypothetical marketing actions** plus a validation checklist.
- Upload a CSV locally (nothing is transmitted to a server).
- Download a plain-text decision brief.
- Restore illustrative demo data.

## Data contract

CSV must have these headings:

```csv
date,team,interest
2025-09-01,Kansas City Chiefs,42
2025-09-08,Kansas City Chiefs,49
2025-09-01,San Francisco 49ers,31
2025-09-08,San Francisco 49ers,38
```

Each date must be ISO format `YYYY-MM-DD`, and each interest number must be between 0 and 100. Provide at least eight observations per team for momentum. The CSV parser is deliberately minimal and does not support commas within quoted values.

**Important:** Teams should share a consistent Google Trends query, period, geographic scope, and normalized comparison scale. Independent 0–100 downloads do not necessarily support direct cross-team comparisons. Google Trends measures *relative search interest*, not actual fandom, website engagement, demand, purchases, or revenue.

## Logic and limitations

Momentum is computed as `mean(last 4 observations) − mean(previous 4 observations)` **in index points**:
- Rising: >= +10 points
- Cooling: <= -10 points
- Stable: otherwise

The app does **not** claim causal attribution, predictions, geographic localization, or a live feed. Its initial built-in data is **invented solely to demonstrate the user experience**, not historical findings. Load your own appropriately sourced dataset before interpreting any specific team result.

## Product framing

1. **Research layer (existing project):** collect, plot, and interpret Google Trends interest.
2. **FanSignal MVP (this folder):** make the signals explorable and translate them into explainable *testable hypotheses*.
3. **Future integrations:** real historical trends export, sports-event overlays, data refresh pipeline, regional interest, and campaign outcome measurement.

This separation keeps the source analysis intact while demonstrating an end-to-end product management story: question → evidence → insight → decision hypothesis → validation.
