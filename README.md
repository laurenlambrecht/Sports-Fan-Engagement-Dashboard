# Sports Fan Engagement Dashboard → FanSignal

**From audience research to a B2B sports marketing intelligence product.**

This project began as an analysis of NFL-related Google search trends and evolved into **FanSignal**, a browser-based prototype designed for sports teams' marketing, content, and growth professionals.

The original analysis asks **when does fan interest change?** FanSignal builds a product layer on top of that research to explore **what could a team do next?**

> **FanSignal is a product prototype, not a live analytics service.** Its default dashboard and sample CSVs use explicitly illustrative data. Upload properly normalized, independently sourced data to explore real patterns.

## Explore FanSignal

**[View FanSignal application files](fansignal/)** · **[Open the app's HTML source](fansignal/index.html)** · **[Read the product guide](fansignal/README.md)**

**Try the interactive prototype (no programming required):**

1. From the [FanSignal development branch](https://github.com/laurenlambrecht/Sports-Fan-Engagement-Dashboard/tree/feature/fansignal-product-layer), select **Code → Download ZIP**.
2. Unzip the folder and open `fansignal/index.html` in Chrome, Safari, or another modern browser.
3. Switch NFL teams, inspect audience-momentum metrics, explore geographic examples, view campaign suggestions, and export a Word-compatible decision brief.
4. For CSV testing, use the included [sample search data](fansignal/sample-data.csv) and [sample regional data](fansignal/sample-geography.csv).

**Note:** The links above open repository files, not a hosted website. A public one-click browser demo requires enabling GitHub Pages or another static hosting service. The application has not yet been verified as publicly deployed.

## FanSignal | B2B product concept

### The problem

Sports organizations have access to audience signals, but raw search-interest charts do not directly tell marketers **where to focus attention, when to activate campaigns, or how to evaluate opportunities**. Translating analytics into a business decision is a separate workflow.

### The solution

FanSignal prototypes an **audience-intelligence and marketing decision-support workspace** for:

- **Team marketing & growth teams:** identify potential windows for content or campaign experiments.
- **Content & social teams:** understand relative attention shifts and adjust editorial planning.
- **Partnership & strategy teams:** explore team and geographic interest as inputs to future hypotheses.

**Product workflow:** Explore interest → interpret momentum → compare contexts → propose an experiment → export a decision brief.

### Features in the current prototype

| Capability | What a team can do |
| --- | --- |
| Audience Momentum Tracker | Examine indexed search-interest series and four-observation momentum classifications. |
| Geographic Discovery | Explore a state-level tile heatmap and optionally upload regional search-interest data. |
| Event Context | View illustrative season-calendar references alongside the analytical workflow; not verified causal explanations. |
| Campaign Opportunity Engine | Receive rule-based, explainable suggestions for marketing experiments and validation KPIs. |
| Competitor Benchmarking | Compare selected teams and review index rankings where data uses a common normalized scale. |
| Exportable Decision Brief | Download an editable Word-compatible document summarizing insights, hypotheses, and validation steps. |

**Current product scope:** standalone HTML, CSS, and JavaScript; browser-local CSV uploads; no backend, account system, live Google Trends API, predictive model, or campaign outcome measurement.

## The research foundation

### Research question

How does interest in NFL-related teams and major events fluctuate during a season, and what patterns might be useful for content timing and marketing strategy?

### Methodology

- Collected Google Trends search-interest data using Python and `pytrends`.
- Visualized changes in relative search interest over time.
- Compared attention patterns around major events, league-wide topics, and selected teams.
- Explored how those patterns might inform sports media and marketing hypotheses.

### Findings from the original analysis

- Super Bowl search interest exhibited a sharp, short-lived spike relative to baseline NFL topics.
- League-level search interest appeared steadier than individual team-interest series.
- Later-season and playoff periods corresponded with stronger search attention in the analyzed series.

These are descriptive patterns in **relative search interest**, not direct measurements of fan engagement, causality, purchase intent, or campaign effectiveness.

## How the two layers fit together

| | Original research | FanSignal product layer |
| --- | --- | --- |
| Goal | Understand search-interest patterns | Help marketers interpret signals and plan tests |
| User | Analyst / researcher | Sports marketing, content, and strategy teams |
| Output | Analysis, plots, and observations | Interactive exploration, recommendations, decision brief |
| Data | Historical Google Trends research | Built-in illustrative demo or user-uploaded CSVs |

The original research remains intact; **FanSignal is an additional interface and decision-support layer**, developed separately in the `fansignal/` directory.

## Running the original analysis

Install dependencies where a compatible requirements file is present and launch Jupyter:

```bash
pip install -r requirements.txt
jupyter notebook
```

For the browser-based FanSignal prototype, there is **no installation step**: open `fansignal/index.html` after downloading the project.

## Limitations and next steps

FanSignal currently includes synthetic demonstration values for additional teams and geographic examples. Team-to-team comparisons require a shared Google Trends normalization basis; state interest must be obtained from separate regional data. Calendar context should not be interpreted as a verified cause of attention shifts.

Next steps include importing verified historical datasets, adding documented team-specific event overlays, testing campaign-planning workflows with intended users, and deploying the prototype to a public URL for recruiters and collaborators.

---

**Focus areas:** Product management · B2B SaaS prototyping · Data analytics · Sports technology · Consumer insights · Marketing strategy
