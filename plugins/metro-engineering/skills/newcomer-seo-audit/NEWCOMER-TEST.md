# Newcomer queries and the newcomer test

## Query list

The query list is the base of the audit. Write 30 to 50 questions a stranger types before a first visit. Put each in one of four stages. Find the page that should answer it. Check whether that page ranks.

| Stage | Example queries | Page that should answer |
| --- | --- | --- |
| Discover | church in East Falls, church near Cherry Hill, reformed church Philadelphia | Campus pages, homepage |
| Evaluate | what do reformed churches believe, is Metro Church legit, church with kids ministry | About, beliefs, kids |
| Plan a visit | Metro Church service times, Metro Church parking, what to wear to church | Plan a visit, campus pages |
| Brand | Metro Church, Metro Church Philly, Metro sermons, RE:NEW Metro | Homepage, sermons, ministry pages |

Search Console regex filters to pull each stage. Adjust the words to the real data.

```
Discover:     (church|churches).*(near|in|around).*(east falls|cherry hill|philadelphia|philly)
Evaluate:     (what|is|do|does|why).*(reformed|presbyterian|church|believe)
Plan a visit: (service|times|parking|kids|dress|wear|first time|visit)
Brand:        (metro|metrophilly)
```

Compare the real queries to the list. Add any real query that was not predicted. Those are the best finds.

## The newcomer test

This is the one check that comes from neither the team nor an LLM. Run it once before the fixes and once after.

1. Find five people who have never visited Metro and do not work or serve here.
2. Give each person a phone and a private browser window. Do not coach.
3. Ask them to do three tasks, one at a time, out loud: find the service time for the nearest campus, find out what happens with a young child, and decide whether they would visit and say why.
4. Record the time, the page where they got stuck, and any word they did not understand.
5. Count success as finishing a task in under 90 seconds with no help.

A task that fewer than 4 of 5 people finish is a gap, whatever the checklist scored.

## The first visit question

Add one question to the connect card and the first visit form: "How did you first find Metro?" Offer these answers: Google search, Google Maps, a friend, social media, an AI assistant, other. Review it each month. It shows which pages and channels really bring people in.

## Rerun schedule

| When | What to run | Outside check |
| --- | --- | --- |
| Day 0 | Baseline: query list, crawl, local search, AI answers, newcomer test, checklist scores. Save every export. | Search Console exports saved. Rich Results Test run on pages with markup. |
| Day 28 | Rerun the query list and crawl after the first fixes. | Search Console impressions and clicks for fixed pages, compared with the baseline. |
| Day 90 | Rerun everything. Run the newcomer test with five new people. | Search Console, CrUX field data, map pack results and first visit survey answers. |

Every month: read the first visit survey answers and note which channel and which page brought people in.
