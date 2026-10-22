# Sports Fan Engagement Dashboard

This analytic project analyzes how fan engagement around sports content changes across a season using **Google Trends** as a proxy for audience interest. It explores how performance, timing, and major moments correlate with spikes in attention, surfacing insights relevant to **sports media, marketing, and digital strategy** teams.


## FanSignal | B2B Product Extension

Building on this initial research, I developed FanSignal, a B2B sports audience intelligence platform designed to help professional sports teams translate fan-interest data into actionable marketing decisions. The interactive prototype combines audience momentum tracking, geographic insights, competitor benchmarking, and campaign recommendations to help teams identify opportunities and develop data-driven strategies.

Live Link: [FanSignal](https://laurenlambrecht.github.io/Sports-Fan-Engagement-Dashboard/fansignal/)

## What this answers
- How does audience interest fluctuate over time?
- Which teams/players/topics drive the biggest spikes?
- What patterns could inform content timing and editorial strategy?

## Method
- Pull search interest data with `pytrends` (Google Trends)
- Visualize trends over time
- Identify peak moments and compare relative attention across terms


## Key Findings
- Fan interest in the Super Bowl exhibits an extreme, short-lived spike relative to baseline league and team interest, highlighting the outsized impact of tentpole events on audience attention.
- League-wide interest (NFL) remains relatively stable throughout the season, while team-specific interest shows higher volatility tied to performance and narrative context.
- Engagement accelerates during late-season and playoff periods, reinforcing the importance of timing content, campaigns, and product launches around high-stakes moments.

## How to run
```bash
pip install -r requirements.txt
jupyter notebook


---

## FanSignal — new product layer (prototype)

**[Explore FanSignal](fansignal/index.html)** · [Product documentation](fansignal/README.md)

FanSignal is an **additional audience-intelligence web application built on top of this research**, not a replacement for the original analysis. While the original project investigates *when* NFL search interest changes, FanSignal prototypes a decision-support workflow for marketers: explore team trends → classify momentum → develop testable campaign recommendations → export a decision brief.

The standalone web prototype supports team comparisons and local CSV uploads. **Its built-in dataset is illustrative, not real NFL historical data.** Recommendations are transparent hypotheses rather than predicted results, and Google Trends is only a proxy for audience attention. See the [FanSignal README](fansignal/README.md) for data requirements and limitations.
