---
name: expert-audit
description: Run an audit the way a senior professional in the field would, from raw source data with named methods and outside validation, not a generic AI review. Use when the user asks to audit, review, gap-analyze or assess something (an SEO page, a design system, a Linear workspace, a codebase, a process) or says "what would a top professional do", "use raw source material", "how would we validate this", or "audit this like an expert". Trigger on audits of Metro pages, tools and workflows even when the user does not use the word "expert".
---

# Expert audit

An audit built from a model's general knowledge reads well and proves little. This method forces the audit onto real data and real checks.

## Step 1: Reflect before you touch anything

Answer four questions in a short plan. Keep each answer concrete.

1. What would a top professional in this field do differently from a generic AI review?
2. What is the rawest source material? Name it. Prefer the page HTML over a tool summary, the crawl over a screenshot, the repo over its docs, live issue data over a best practices list.
3. Which exact methods and tools will you use? Name them, for example regex filters in Search Console, computed styles from a live crawl, WCAG contrast math, a query against live Linear data.
4. What evidence, other than you and the user, would show the findings are right? Name it, for example Search Console, the Rich Results Test, GA4, a rerun of the baseline, or a fresh agent rebuilding from the documentation.

Then restate the original request as a prompt that asks for exactly that. If the user already gave this prompt, use it.

For expensive audits (a crawl, many tool calls, many files), show the plan and wait for "go". For a small audit with the data in hand, proceed.

## Step 2: Gather raw data

Collect the raw material and keep it. Write scripts for counting, parsing and measuring, and run them. Do not estimate figures in prose.

When a tool or source is blocked, say so in the report. Examples are an API plan that returns "insufficient plan", a site the workspace cannot reach, or a viewport that did not finish. Ask the user to attach the raw file or run the step locally. Never fill a gap from memory and present it as a measurement.

Treat reference material, such as another design system or a best practices list, as a lens and not as the benchmark. The organization's own rules rank first. Validate any proposed view, filter, rule or workflow against live data before you trust it, because generic advice often breaks on real data.

## Step 3: Report

Open with the baseline metrics so the user can rerun them later. Then list the gaps ranked by impact. Each gap has four parts: the evidence, the proposed fix, the metric that confirms the fix worked, and the named outside check with a future date. Give each finding one of three confidence levels: measured, inferred, or not verified.

Correct your own earlier statements in the report when the data contradicts them. State what you could not measure.

Public facts that matter, such as speaker names, titles and dates, get a live search, and any mismatch is reported.

## Step 4: Close

One sentence on the result, the document or file, and the single next action. Offer to make the fixes. Do not make changes to live systems until the user confirms.
