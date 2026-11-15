---
name: newcomer-seo-audit
description: Audit metrophilly.org pages as a professional local-SEO and conversion auditor, judging each page by whether a stranger can find it, find it useful, understand it and decide to visit East Falls or Cherry Hill. Use when the user asks for an "SEO audit", "newcomer audit", "page checklist", "is this page optimized for newcomers", "audit our site for first-time visitors", or wants the team checklist or an LLM audit prompt for Metro pages. Also use when scoring one Metro page against the checklist, even if the user never says "SEO".
---

# Newcomer SEO audit

This skill audits metrophilly.org for one outcome: a stranger finds a Metro page, finds it useful, understands it, and decides to visit.

It runs on top of `expert-audit`. Follow that skill's method: raw data, named tools, outside validation, no estimated numbers.

## Files

| File | Use it for |
| --- | --- |
| `CHECKLIST.md` | The 0/1/2 per-page checklist and the site-wide checks. Give this to the team as is. |
| `PROMPTS.md` | The full LLM audit prompt and the per-page scoring prompt. |
| `NEWCOMER-TEST.md` | The five-person newcomer test, the query list template and the first visit survey question. |

Read `CHECKLIST.md` before you score any page. Read the other two files only when you reach their step.

## Rules

1. Work from raw data. Prefer page HTML over a tool summary, a crawl over a screenshot, and Search Console exports over a best practices list.
2. Never estimate a number. If a tool is blocked, say so and ask the user for the export.
3. Label every finding MEASURED, INFERRED or NOT VERIFIED.
4. Score a check only with evidence. No evidence means NOT VERIFIED and a score of 0.
5. Do not change the live site or the CMS until the user confirms.
6. Check every public fact (times, addresses, names, ministry spelling) against the live site and report any mismatch.
7. Write suggested public copy with `metro-copy-voice`: warm full sentences, the visitor as the subject, no em dashes.

## Workflow

### Step 1: Plan, then wait for "go"

Answer in short form:

1. What would a top local-SEO and conversion auditor do here that a generic audit would not? (Newcomer search behavior, local search, page jobs, rendered HTML, AI answers, funnel leaks, insider language.)
2. Which raw sources will you use? Search Console query and page exports, live crawl with raw and rendered HTML, sitemap.xml and robots.txt, Sanity SEO fields, Google Business Profile, real SERPs, GA4, connect card data.
3. Which exact tools and methods will you use? Ahrefs Site Audit, Site Explorer and Search Console tools, a Playwright mobile crawl at 390px, regex query filters, schema validators, PageSpeed Insights and CrUX, contrast checks.
4. What outside evidence will show the results are right? Search Console at 28 and 90 days, the Rich Results Test, CrUX field data, five newcomer sessions, first visit survey data, a baseline rerun.

List every source or tool you cannot reach and what you need from the user. Stop. Wait for "go". For a single page with the data in hand, skip the wait.

### Step 2: Gather

1. Build the newcomer query list (see `NEWCOMER-TEST.md`). Pull impressions, clicks, average position and ranking URL for each query. List queries with no ranking page.
2. Crawl every indexable URL. Record status, canonical, title, meta description, H1, word count, raw versus rendered text, internal links in and out, schema types, text above the fold at 390px, and LCP and CLS from field data first.
3. Audit local search for each campus: Google Business Profile, Apple Maps, name, address and phone consistency, map results for 10 local queries.
4. Test 10 newcomer questions in ChatGPT, Google AI Overviews and Perplexity. Record whether Metro is named, which URL is cited, and any wrong fact.
5. Check Sanity for empty SEO fields, duplicate slugs and draft versus published mismatches.

### Step 3: Score each page

1. Give the page one job: find, trust, understand or visit.
2. Read the page as a first-time visitor on a phone. Write what you understand in one sentence. If you cannot, score U1 as 0.
3. Score every check in `CHECKLIST.md` with 0, 1 or 2. Attach evidence and a confidence label to each score.
4. Apply the fail rule: any 0 in F4, U1, U3 or V1 fails the page.
5. Write up to three fixes ranked by impact on a newcomer. Give each fix the metric that will show it worked.

### Step 4: Report

1. Baseline metrics first, so the user can rerun them: share of newcomer queries with a ranking page, indexable pages, pages with empty SEO fields, mobile Core Web Vitals pass rate, map pack presence, AI answers that name Metro.
2. Gaps ranked by impact on a newcomer. Each gap has the evidence, the fix, the metric that confirms it, and the outside check with a date.
3. What you could not measure.
4. A correction of any earlier claim the data contradicts.
5. A script or export so the baseline can be rerun.

### Step 5: Close

One sentence on the result, where the document is, and the single next action. Offer to make the fixes. Do not touch live systems until the user confirms.

## Validation

A finding is confirmed only when one source outside the audit agrees: Search Console, a validator, field data, a newcomer, or survey data. Rerun the baseline at 28 and 90 days.

Use the model as a second reviewer, not the judge. It cannot see a live phone screen, hear a stranger's confusion or know whether a time is stale. When the model and a human score a check differently, open the evidence and decide who is right.
