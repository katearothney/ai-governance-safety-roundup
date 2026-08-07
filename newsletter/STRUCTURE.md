# How every edition is structured

Every weekly edition of Governance Signals follows the same shape, so they stack up into something a reader can follow week after week. Start from [`_TEMPLATE.html`](_TEMPLATE.html), fill in the brackets, and keep the section order.

## The shape

1. **Masthead**, the brand, the byline, the week, and a rough read time.
2. **Cover headline**, the single biggest story of the week, plain and specific. Not a grand monthly thesis, just what mattered most this week.
3. **This week in 60 seconds**, three or four bullets, then the one-sentence throughline that ties the week together.
4. **01 Policy and regulation**, what moved on rules, with a plain-terms explainer under each item.
5. **02 Company watchlist**, a pass over the labs, clouds, and compute players. Note who moved and who went quiet.
6. **03 Startups (Series D and below)**, governance, observability, evals, agent frameworks, AI safety, responsible AI.
7. **04 Trends moving this week**, only the throughlines the news actually bent, pulled from `landscape/trends/`.
8. **05 Compete and whitespace**, the five forces read, and the open lane nobody has claimed.
9. **06 Data**, a quant stat table and one or two qualitative quotes.

## The two rules that make it credible

**Explain the substance, do not just report it.** When a rule or product shows up, say what it actually requires or does, in plain terms. A reader should learn what Article 50 is (disclosure and machine-readable content provenance), not just that it went live. Use the light-blue explainer box (`.plain`) for this.

**Split the sources.** On the items that matter, give two links:

- **Primary**, the regulator or company itself (the EU AI Office, a company's own page). This is where a reader verifies the claim at the source.
- **Coverage**, a news or analysis outlet's take (Reuters, a law-firm alert, a trade outlet). This is how the claim is being read.

Write it inline like this: `(Primary: <a>EU AI Office</a>. Coverage: <a>Gibson Dunn analysis</a>.)`

## Voice and hygiene

- No em dashes. No semicolons. First person, present tense, concrete words.
- Every number and every quote links to its source. Where a read is a guess, the sentence says so.
- Never invent a quote, a statistic, or a URL.

## Naming and cadence

- File name: `YYYY-MM-DD-governance-signals.html`, dated by the Monday of the week.
- Add each new edition to the top of the index in [`README.md`](README.md).
- Cadence is weekly. The material comes from the framework: [news](../landscape/news/), [trends](../landscape/trends/), [compete-whitespace](../landscape/compete-whitespace.md), and [data](../data/).

## How it gets generated

The `market-radar-roundup` skill drafts an edition against this template from the framework content, runs the voice and hygiene checks, and saves it here ready to commit.
