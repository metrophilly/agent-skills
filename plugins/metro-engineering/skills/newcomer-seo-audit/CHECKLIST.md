# Newcomer SEO checklist

Score every check 0 (fail), 1 (partial) or 2 (pass). Write evidence for every score: a URL, a screenshot, a number or a quoted line. A score without evidence does not count.

Test pages on a phone, 390px wide.

## Page jobs

Give each page one job before you score it.

| Job | Typical pages | Success test on a phone, in 10 seconds |
| --- | --- | --- |
| Find | Homepage, campus pages | A stranger sees what Metro is, where it is, when it meets and one next step. |
| Trust | About, beliefs, staff, history | A stranger sees real people, a real address and what we believe, in plain words. |
| Understand | Sermons, ministries, events | A stranger can say in one sentence what this is and who it is for. |
| Visit | Plan a visit, kids, directions | A stranger knows where to go, what time, what happens first, and taps once to plan. |

## Per-page checks

| ID | Area | Check | Pass (2) looks like |
| --- | --- | --- | --- |
| F1 | Findability | A newcomer query leads to this page. | The page ranks on page 1 for at least one query from the query list. |
| F2 | Findability | The title tag is plain and campus specific where needed. | Under 60 characters, names what the page is, names East Falls or Cherry Hill if the page is campus specific. |
| F3 | Findability | The meta description invites a visit. | One or two warm sentences with a concrete detail, such as a time or a place. |
| F4 | Findability | The page is indexable and canonical. | Returns 200, has a self canonical, no noindex, appears in sitemap.xml. |
| F5 | Findability | Other pages link here. | At least two relevant internal links in, with descriptive link text. |
| U1 | Usefulness | A stranger knows what the page is in 10 seconds. | Headline and first paragraph say what this is and who it is for, above the fold at 390px. |
| U2 | Usefulness | One clear next step shows above the fold. | A single main button or link, such as Plan your visit. |
| U3 | Usefulness | Time and place are easy to find. | Service times and address show without scrolling on a campus page, and are one tap away elsewhere. |
| L1 | Language | Insider terms are explained. | Names like Advance, RE:NEW or Crossroads carry a plain phrase the first time they appear. |
| L2 | Language | Ministry and event names are spelled the same everywhere. | The name matches its permanent page, in full, every time on the page. |
| L3 | Language | The copy speaks to the visitor. | The searching person is the subject of the sentences. Warm full sentences, no stacked labels. |
| T1 | Trust | The page answers a first-time fear. | It says what happens, how long it lasts, and what to wear or what to expect for kids, if the page is about a visit. |
| T2 | Trust | Real people and real places show. | A real photo, a named person or a street address, not stock images only. |
| V1 | Visit path | A visit is one tap away. | The plan a visit page is reachable in one tap from this page. |
| V2 | Visit path | The page links to the right campus. | The East Falls or Cherry Hill link matches the page content. |
| C1 | Campus accuracy | Facts match the campus. | Floors, entrances, parking and times were checked against that campus, not copied from the other. |
| X1 | Technical | The text is in the rendered page. | The main text appears in the raw HTML or in the rendered DOM within 3 seconds. |
| X2 | Technical | The mobile page is fast and stable. | Field data (CrUX) shows LCP under 2.5 s and CLS under 0.1. |
| X3 | Technical | Structured data is valid. | Church, Event or VideoObject markup passes the Rich Results Test where it applies. |
| X4 | Technical | Images have useful alt text. | Every meaningful image has alt text that describes it. |
| X5 | Technical | The page is accessible. | Text contrast is at least 4.5 to 1, and a keyboard can reach every link and button. |

Fail rule: a page with any 0 in F4, U1, U3 or V1 fails, whatever its total. Those four checks decide whether a stranger can use the page at all.

## Site-wide checks

Run these once for the whole site. Most newcomers meet a church on a map or in an AI answer before they meet its website.

| ID | Area | Check | How to test | Pass looks like |
| --- | --- | --- | --- | --- |
| S1 | Local search | Each campus has a complete Google Business Profile. | Search "Metro Church East Falls" and "Metro Church Cherry Hill" in Google Maps on a phone. | Correct name, address, hours, website link, photos and category for both campuses. |
| S2 | Local search | Name, address and phone match everywhere. | Compare the website footer, Google, Apple Maps and one directory. | Identical spelling and format in every place. |
| S3 | Local search | The campus shows in the map pack. | Search 10 local queries, such as "church near East Falls", in a private window. | Metro appears in the top 3 map results for at least half of them. |
| S4 | AI answers | AI tools name Metro correctly. | Ask 10 newcomer questions in ChatGPT, Google AI Overviews and Perplexity. Record name, cited URL and any wrong fact. | Metro is named for local questions, the cited URL is right, and no fact is wrong. |
| S5 | Crawl | Every important page is in the sitemap and returns 200. | Open /sitemap.xml and /robots.txt. Crawl with Ahrefs Site Audit. | No broken pages, no accidental noindex, no redirect chains longer than 1. |
| S6 | Crawl | Raw HTML matches the rendered page. | View source, then compare it to the rendered DOM in Playwright for 10 pages. | Main text, headings and links appear in the raw HTML. |
| S7 | CMS | No page has empty SEO fields. | In Sanity, list pages with an empty title, description or image alt. | Zero empty fields on indexable pages. |
| S8 | CMS | No draft or duplicate slug is live. | Compare published documents to the sitemap. | One live URL per page, no draft text published. |
| S9 | Search Console | The newcomer queries have a ranking page. | Export queries and pages. Filter with the query list. | Every newcomer query has a page that ranks, or it goes on the gap list. |
| S10 | Search Console | Brand queries lead to the right page. | Filter queries that contain "metro" and the campus names. | The campus pages rank first for their own name. |
| S11 | Language | Ministry names are consistent across the whole site. | Search the site for each ministry name and its misspellings. | One spelling, one capitalization, full name every time. |
