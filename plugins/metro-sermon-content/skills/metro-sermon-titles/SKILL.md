---
name: metro-sermon-titles
description: "Generate sermon title options for Metro Church (Philadelphia) videos, in Metro's established title format. Use this whenever the user asks for \"sermon title ideas,\" \"title options,\" \"what should we call this sermon,\" or wants YouTube/Instagram title copy for a sermon — whether from a full transcript, a sermon summary, or just a passage + theme. Also trigger as a proactive follow-up after generating a Metro sermon description. Distinct from metro-sermon-description (which produces the full video description) — use this skill specifically when titles are the ask, even if a description was already generated earlier in the conversation."
---

# Metro Church Sermon Titles

Generate sermon title options for Metro Church's YouTube/Instagram video library, in Metro's house format.

## The single most important rule

**Only pull from what the pastor actually preached.** Draw the hook from the sermon's own central question or its most vivid, specific image as it appears in the transcript/summary — never generic phrasing, never an image or theme you're supplying yourself. If a passage, series, or sermon title fact isn't available, leave it as a placeholder rather than inventing it.

## Format

```
[Hook statement or question] (Passage — Sermon: "Sermon Title")
```

If there's no known title, drop the title clause:

```
[Hook statement or question] (Passage — Sermon)
```

Use an em dash ("—") between the passage and "Sermon" — this is the one place an em dash is used in Metro sermon copy. Passage ranges use an en dash (e.g. "Jonah 4:1–11").

**Examples:**
- How To Taste and See That God is Good (John 2:1–11 — Sermon: "The Gospel: The First Miracle")
- What Is Sin and Where Do We Find Hope From It? (Genesis 3:7–24 — Sermon: "The Gospel: The Redeemer")
- Why We Create, Build, and Long for More (Genesis 1:1–2; 1:26–2:3 — Sermon)
- What God Means When He Says He Will Prosper You (Jeremiah 29:1–14 — Sermon: "City: The Planter")

## Generating the hook

- Draw from the sermon's central question, tension, or its most specific, vivid image (a withered vine, six stone jars, a flaming sword) — not a generic restatement of the topic.
- Both statements and questions are fair game; mix the two across the set.
- Title-case the hook.
- Avoid churchy jargon a first-time YouTube viewer wouldn't parse.

## Output

Generate 5–7 options per request. After the list, briefly flag:
- Which option(s) are **strongest for SEO** — phrasing close to how someone would actually type a real search or felt-need question (e.g. "why do I feel..." / "what does the bible say about...").
- Which option(s) are **strongest for click appeal** — built on the sermon's most specific, curiosity-driving image or turn, unique to this sermon.
- Offer to generate more in a particular direction (more question-based, more image-driven, etc.) if asked.

## Working with the source material

The user may hand you a full transcript, a sermon description already generated, or just a passage + brief theme. Work with whatever's given — don't ask for a full transcript if a summary is enough to identify the passage, structure, and central image. If the passage, series name, or sermon title itself isn't known, leave that piece as a bracketed placeholder rather than guessing.