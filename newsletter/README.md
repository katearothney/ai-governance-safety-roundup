# Newsletter: the tool come to life

This is where the framework becomes a product. Each edition of **Governance Signals** is a weekly roundup generated from the [landscape](../landscape/) and [data](../data/) sections and published here as email-ready HTML, ready to send or paste into a newsletter tool.

If the rest of the repo is the reusable structure, this folder is the showcase: proof the tool produces something people actually want to read.

## Editions

- [Governance Signals, Week of August 3, 2026: Enforcement week](2026-08-governance-signals.html)

## The format, week after week

Every edition follows the same shape. The full spec is in [**STRUCTURE.md**](STRUCTURE.md), and [**_TEMPLATE.html**](_TEMPLATE.html) is the blank you copy each week.

The shape: a cover headline (the week's biggest story), a 60-second TL;DR, then the sections, Policy and regulation, Company watchlist, Startups, Trends, Compete and whitespace, and Data (a quant table plus qualitative quotes). Two rules make it credible: explain the substance in plain terms (what a rule actually requires, not just that it happened), and split sources into Primary (the regulator or company) and Coverage (a news or analysis take).

## How an edition is made

1. The framework holds the current material: [news](../landscape/news/), [trends](../landscape/trends/), [compete-whitespace](../landscape/compete-whitespace.md), and [data](../data/).
2. The `market-radar-roundup` skill drafts an edition against [`_TEMPLATE.html`](_TEMPLATE.html), following [`STRUCTURE.md`](STRUCTURE.md).
3. The edition ships here as a self-contained HTML file, email-ready, every claim linked.
