# How every edition is structured

Every weekly edition of Governance Signals follows the same shape, so they stack up into something a reader can follow week after week. Start from [`_TEMPLATE.html`](_TEMPLATE.html), fill in the brackets, and keep the section order.

## The shape

1. **Masthead**, the brand, the byline, the week, and a rough read time.
2. **Cover headline**, the single biggest story of the week, plain and specific. Not a grand monthly thesis, just what mattered most this week.
3. **This week in 60 seconds**, three or four bullets, then the one-sentence throughline that ties the week together.
4. **01 Policy and regulation**, what moved on rules, with a plain-terms explainer under each item.
5. **02 Incidents and safety**, breaches, eval failures, real-world harm, allegation kept separate from proven fact.
6. **03 Company watchlist**, a pass over the fixed core roster (see `../landscape/news/2-company-watchlist.md`). Write a company up only when its news touches the lens. Collapse the quiet ones into one line. A rotation bench appears only on significant news.
7. **04 Startups (Series D and below)**, governance, observability, evals, agent frameworks, AI safety, responsible AI. Skip if nothing moved.
8. **05 Trends**, the throughlines this week's stories organically surfaced, and how the week builds on earlier editions. Not a fixed checklist.
9. **06 On the radar**, the forward calendar. Upcoming deadlines, comment periods, expected releases, hearings, and events, dated where known. This is the section readers forward to their teams, so keep it concrete and current.
10. **07 Deep dive**, one durable concept explained in about 150 words (content provenance, ISO 42001, agent sandboxing, an eval method). Gives the edition lasting reference value beyond the news.
11. **08 Data**, a quant stat table of fresh numbers not already used in the body, plus a short qualitative read of how the week is being framed.

Two things run through the news items and matter as much as the sections:

- **Tag every item by area.** Governance, Safety, Security, Observability, or Responsible AI, so each reader can scan their slice.
- **End every item with what it means.** A concrete, specific implication for the relevant persona (product marketer, product manager, researcher, policy lead). Not "lead with trust," but the actual move. This is the point of the newsletter, converting news into a decision.

## The rules that make it credible

**Keep the news to the past seven days.** Every item in the news sections (Policy and regulation, Incidents and safety, Company watchlist, Startups) must have happened in the last seven days. Cut anything older, even if it is interesting. Two exceptions. One, the Trends section can build on longer-running developments, since that is its whole job, and it should date the older items so the reader sees the arc. Two, inside a this-week item you can reference something older when it is the direct background to the news you are covering (for example, noting a June executive order when the news is this week's meeting about it). The test: is the news itself from the past seven days? If yes, older context is fine. If the news itself is old, cut it.

**Name the actor.** Never write "Washington," "the US," "Brussels," or "the government" when you can name the specific office, official, or administration behind a move. Not "the US finalized voluntary tests," but "the Trump administration finalized voluntary tests, announced by a White House official." Not "the AI safety chief resigned," but "Chris Fall, director of CAISI, the Commerce Department's AI safety arm, resigned." The specificity is what makes it read like reporting instead of a summary. If you cannot verify the name or office, say so rather than staying vague or guessing.

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
