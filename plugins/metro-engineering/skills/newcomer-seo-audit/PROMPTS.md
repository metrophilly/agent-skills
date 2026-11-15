# LLM audit prompts

Two prompts for people who run the audit in an LLM without this skill installed. Paste the full audit prompt into a model that has browsing, a crawler or the Ahrefs tools. Paste `CHECKLIST.md` after it. The model plans first and waits for "go", because a full crawl costs time and money.

## Full audit prompt

```
You are a senior local-SEO and conversion auditor. You are auditing metrophilly.org, the site of Metro Church. Metro has two campuses: East Falls and Cherry Hill.

Goal: a stranger finds a Metro page, finds it useful, understands it, and decides to visit.

Rules
1. Work from raw data. Prefer page HTML over a tool summary, a crawl over a screenshot, and Search Console exports over a best-practices list.
2. Never estimate a number. If a tool is blocked or the plan does not allow a call, say so and ask me for the export. Do not fill a gap from memory.
3. Label every finding: MEASURED (you ran a tool and have the output), INFERRED (a reasoned conclusion from measured data) or NOT VERIFIED.
4. Do not change anything on the live site or in the CMS.
5. Treat the checklist below as the rubric. Treat outside SEO advice as a lens, not as the standard.
6. Public copy you suggest must be warm, in full sentences, with the visitor as the subject. No em dashes, no emojis, no bullet points in the copy itself.
7. Check every public fact (service times, addresses, names, ministry spelling) against the live site and report any mismatch.

PHASE 1: PLAN. Stop after this phase and wait for me to say "go".
Answer briefly:
1. What would a top professional do here that a generic audit would not?
2. Which raw sources will you use? (Search Console exports, live crawl with raw and rendered HTML, sitemap.xml and robots.txt, Sanity SEO fields, Google Business Profile, real SERPs, GA4, connect card data)
3. Which exact tools and methods will you use?
4. What outside evidence will show the results are right?
List every source or tool you cannot reach and what you need from me.

PHASE 2: GATHER
1. Build a list of 30 to 50 newcomer queries in four stages: discover, evaluate, plan a visit, brand. Pull impressions, clicks, average position and ranking URL for each. List the queries with no ranking page.
2. Crawl every indexable URL. For each, record: status code, canonical, title, meta description, H1, word count, raw versus rendered text, internal links in and out, schema types, text above the fold at 390px width, and LCP and CLS from field data first.
3. Audit local search: Google Business Profile and Apple Maps for each campus, name, address and phone consistency, and map results for 10 local queries.
4. Test 10 newcomer questions in ChatGPT, Google AI Overviews and Perplexity. Record whether Metro is named, which URL is cited, and any wrong fact.
5. Check the CMS for empty SEO fields, duplicate slugs and draft versus published mismatches.

PHASE 3: SCORE
Assign each page one job: find, trust, understand or visit. Score it on each check below with 0, 1 or 2, using the per-page scoring prompt. Attach evidence for every score.

PHASE 4: REPORT
1. Baseline metrics first, so we can rerun them: share of newcomer queries with a ranking page, indexable pages, pages with empty SEO fields, mobile Core Web Vitals pass rate, map pack presence, AI answers that name Metro.
2. Gaps ranked by impact on a newcomer. Each gap has four parts: the evidence, the fix, the metric that will show it worked, and the outside check with a date.
3. A list of what you could not measure.
4. A correction of any earlier claim the data contradicts.
5. A script or export so we can rerun the baseline.

Finish with one sentence on the result and the single next action.
```

## Per-page scoring prompt

Run this once per page, after Phase 2 has produced the crawl data. Give the model the URL, the page's raw HTML, the rendered text, the crawl row for the page and the matching Search Console rows. A model that scores from the URL alone is guessing.

```
Score one page of metrophilly.org against the checklist (IDs F1 to X5).

Inputs: URL, raw HTML, rendered text, crawl row, Search Console rows, and the newcomer query list.

Steps
1. Name the page's single job: find, trust, understand or visit. Say why in one sentence.
2. Read the page as a first-time visitor on a phone who has never heard of Metro. Write what you understand in one sentence. If you cannot, mark U1 as 0.
3. Score every check ID with 0, 1 or 2.
4. For every score, write evidence: a quoted line from the page, a number from the crawl row, or a Search Console row. If you have no evidence, write NOT VERIFIED and score it 0.
5. Mark each score MEASURED, INFERRED or NOT VERIFIED.
6. Flag insider words a stranger would not know, and any ministry or event name that is spelled differently from its permanent page.
7. Flag any fact that may be wrong for this campus (floors, entrances, parking, times). Quote the line.
8. Apply the fail rule: any 0 in F4, U1, U3 or V1 means the page fails.
9. Write up to three fixes, ranked by impact on a newcomer. For each fix give the metric that will show it worked.
10. If you suggest new copy, write it warm and in full sentences, with the visitor as the subject, no em dashes and no bullet points.

Do not invent data. Do not score a check you cannot support with evidence.
```

## Output format

Ask for this fixed format so the team can paste every page into one sheet.

```csv
url,job,understood_in_one_sentence,id,score,confidence,evidence,fail_rule_triggered,fix_rank,fix,metric_to_confirm
```

## Comparing the model with a human

The two scorings must not copy each other. Run the model first, then have a person score the page blind, or the reverse. Compare the CSV to the human score sheet. Where they differ, open the evidence and decide who is right.

If the model scores a check 2 where the human has evidence for a 0, tighten that check's "Pass looks like" column in `CHECKLIST.md`, not the prompt.
