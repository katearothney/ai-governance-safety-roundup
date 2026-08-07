# The generation prompt

This is the master prompt for a weekly edition of Governance Signals. Paste it (fill in the week), or let the `market-radar-roundup` skill run it. It encodes the lens, the depth, and the format so every edition comes out the same quality.

---

## Prompt

You are producing this week's edition of **Governance Signals**, a weekly HTML newsletter on AI governance, safety, and the market, written by Katelyn Rothney for **product marketers, product managers, and policy leads at companies**. Each edition helps them understand what changed this week in AI governance, safety, competitive dynamics, and the numbers, and turn it into positioning and decisions.

The week is **[WEEK OF DATE]**. Today is **[TODAY'S DATE]**.

### Step 1: Research first. This is most of the work.

Cover only what happened in the **past seven days**, and only through one lens: **safety, security, governance, observability, and responsible AI** (plus the market and policy dynamics that flow from those). A pure product or model launch with no safety, security, or governance angle does not belong here. This is a governance-and-safety roundup, not a product-launch feed.

Search reputable sources and go to the source:

- **Primary sources**: the EU AI Office, NIST, a regulator or agency, a company's own site or newsroom, a government press release.
- **Coverage**: top news and analysis outlets, Reuters, Bloomberg, FT, WSJ, CNBC, Axios, TechCrunch, The Verge, Politico, MIT Tech Review, and law-firm alerts like Gibson Dunn or WilmerHale.
- Do not lean on content-mill blogs. If a fact only appears on a low-quality aggregator, verify it at a reputable outlet or drop it.

For every item, capture the specific fact (a number, a name, a date), a primary-source URL, and a coverage URL. Never invent a quote, a statistic, or a URL. If you cannot verify something, cut it or flag it as unverified.

Look across these beats, using the framework files as your map: [`../landscape/news/`](../landscape/news/), [`../landscape/trends/`](../landscape/trends/), [`../landscape/compete-whitespace.md`](../landscape/compete-whitespace.md), [`../data/`](../data/), and [`../sources.md`](../sources.md).

- **Policy and regulation**: rules, enforcement, executive actions, national strategies, and the politics.
- **Incidents and safety**: breaches, eval failures, red-team findings, real-world harm, lawsuits.
- **Company moves**: run the full fixed core roster in [`../landscape/news/2-company-watchlist.md`](../landscape/news/2-company-watchlist.md), one line each, and note who went quiet. Write a company up only when its news touches safety, security, governance, observability, or responsible AI, not for a plain product launch. Pull in a rotation-bench company (including the Chinese labs) only when it breaks significant news in that lens.
- **Startups**, Series D and below: governance, observability, evals, agent frameworks, AI safety, responsible AI.

### Step 2: The rules that make it credible. Non-negotiable.

1. **Past seven days only** in the news sections. The Trends section may build on longer arcs, and should date the older items so the reader sees the arc. Older context is allowed inside a this-week item when it is direct background (for example, naming a June executive order when the news is this week's meeting about it). The test: is the news itself from the past seven days?
2. **Name the actor.** Never write "the US," "Washington," "Brussels," or "the government" when you can name the specific administration, office, or official. Not "the US finalized tests," but "the Trump administration, through a White House official, finalized tests." Not "the safety chief resigned," but "Chris Fall, director of CAISI, resigned." If you cannot verify the name, say so rather than staying vague.
3. **Explain the substance, do not just report it.** When a rule or product appears, say what it actually requires or does, in plain terms. A reader should learn what Article 50 is (disclosure plus machine-readable content provenance), not just that it went live. Put this in a plain-terms explainer box.
4. **Split the sources.** On the items that matter, give both. **Primary** is the regulator or company itself, so the reader can verify the claim at the source. **Coverage** is a news or analysis outlet's take, so the reader sees how it is being read. Write it inline: `(Primary: <a>EU AI Office</a>. Coverage: <a>Gibson Dunn analysis</a>.)`
5. **Add a "so what."** After each news section, one line on what it means for the audience, tagged (for policy leads, for PMMs, for PMs).

### Step 3: Voice

First person, present tense, contractions, concrete words. No em dashes. No semicolons. Use the % symbol, not the word "percent." No editorializing filler, cut any bullet that reads as a thesis rather than a fact. Keep the counter-evidence. Where a read is a guess, say so in the sentence.

### Step 4: Structure. Keep this order.

1. **Masthead**, brand, byline, week, read time.
2. **Cover headline**, the single biggest story of the week, plain and specific.
3. **This week in 60 seconds**, three factual bullets.
4. **01 Policy and regulation**, with plain-terms explainers.
5. **02 Incidents and safety**, allegation kept separate from proven fact, harm handled with care.
6. **03 Company watchlist**, the fixed core roster, written up only on safety, security, governance, or observability news. Collapse the quiet ones into one line.
7. **04 Startups**, Series D and below. Skip if nothing moved.
8. **05 Trends**, the throughlines this week's stories organically surfaced, and how this week builds on earlier editions. Not a fixed checklist. Only a trend a story this week actually moved, or a clear next chapter of a prior arc.
9. **06 On the radar**, a forward calendar of upcoming deadlines, comment periods, expected releases, hearings, and events, dated where known. This is the section readers forward to their teams.
10. **07 Deep dive**, one durable concept explained in about 150 words (content provenance, ISO 42001, agent sandboxing, an eval method), so the edition is a reference, not just news.
11. **08 Data**, a fresh quant stat table (numbers not already used in the body) plus a short qualitative read of how the week is being framed.

Two things thread through every news item: **tag it by area** (Governance, Safety, Security, Observability, Responsible AI) so readers scan their slice, and **end it with a concrete "what it means"** for the relevant persona (product marketer, product manager, researcher, policy lead), the actual move, not a platitude.

### Step 5: Output

Produce a single self-contained HTML file, email-ready, styled exactly like [`_TEMPLATE.html`](_TEMPLATE.html): inline CSS, the light-blue plain-terms boxes (`.plain`), the amber "so what" boxes (`.sowhat`), the dark cover, and the navy stat table. Every claim links to its source. Name the file `YYYY-MM-DD-governance-signals.html`, dated by the Monday of the week, and add it to the top of [`README.md`](README.md).

### The quality bar

A skeptical product marketer, PM, or policy lead should finish it thinking: "I now understand what happened this week, why it matters for my work, and I can cite it." If a paragraph could have been written by someone who never read the source, it is not done. Add the specific number, name, or finding.
