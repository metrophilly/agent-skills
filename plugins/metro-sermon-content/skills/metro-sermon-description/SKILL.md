---
name: metro-sermon-description
description: Generate a YouTube/video description for a Metro Church (Philadelphia) sermon from a raw sermon transcript. Use this whenever the user provides a sermon transcript and asks for a "YouTube description," "video description," "sermon description," or wants copy for a sermon video going on YouTube or Instagram. Also use when the user pastes a transcript and references Metro's established description format, asks for sermon title options, or is doing digital content operations for Metro's sermon video library. Trigger even if the user just says "help me with this next sermon" and drops in a transcript — that is the cue.
---

# Metro Church Sermon Description

Turn a raw sermon transcript into a polished YouTube/video description in Metro Church's established house format, plus optional title options. The audience is people encountering the video for the first time on YouTube or Instagram — so the description is both a faithful summary and a warm invitation to watch.

## The single most important rule

**Only pull from what the pastor actually preached.** Do not add your own theological flavor, illustrations, cross-references, or emphases that aren't in the transcript. If the pastor built the sermon on three points, use those three points. If he anchored a claim on a specific text or image (a fig leaf, a flaming sword, six stone jars, a withered vine), use his. When in doubt, stay closer to the transcript, not further. Metro is Reformed, confessional, and gospel-centered; the transcripts already reflect that, so faithful summary preserves the theology without you importing anything.

Scripture references default to the **NIV 1984** translation (Metro's standard). Don't quote scripture at length — paraphrase or reference, and only use wording that appears in the transcript.

## Output structure

Produce the description in this exact order:

1. **Body copy** — 2–3 paragraphs (see "Body copy" below).
2. **Metadata block** — with placeholders for anything not derivable from the transcript.
3. **Boilerplate** — the fixed Metro mission + social block (see "Boilerplate," reproduce verbatim).

Wrap the whole thing so the user can copy it directly. After delivering, ask for the missing metadata (title, preacher, series, air date) and offer title options.

### Body copy

Three paragraphs is the default shape, but two is fine for a shorter deck. The arc:

- **Open with a hook.** Lead with a question or the sermon's own opening framing — the tension or question the pastor himself set up. ("Why does grace make some of us angry?" / "What does it really mean to know who Jesus is?" / "At the source of every experience of suffering...") Don't open with dry setup like "In this sermon we will examine."
- **Walk the sermon's actual movement.** Most Metro sermons have an explicit structure (e.g. "who he is, what he did, what we're supposed to do with it" or "the diagnosis of anger, the root cause, and the cure"). Name it and trace it in the pastor's own terms and images. Land on the gospel turn — the point where the sermon moves to Christ and the cross — because that's where these sermons always resolve.
- **Close with an invitation to watch.** Address the first-time viewer directly: someone who might be "empty, dry, desperate, or simply curious," "exploring Christianity, wrestling with doubt, or seeking encouragement." Invite them to watch. End with a short, plain call like "Take a few minutes to watch" or "watch, and see who Jesus really is." This last move is what separates a description from a pure summary — always include it unless the user explicitly asks for summary-only.

Tone: warm, clear, unhurried, non-clichéd. Reformed and gospel-centered but accessible to a non-churchgoer. Avoid churchy jargon that a first-time YouTube viewer wouldn't parse.

If the user asks for it "shorter," compress to two tight paragraphs; if "less than a summary" or "more of an invitation," strengthen the hook and the closing call to watch.

### Metadata block

Place directly under the body copy. Use an em dash / en dash for the passage range. Fill in the passage from the transcript (the reader almost always states it up front). Leave bracketed placeholders for the rest — these are never in the transcript:

```
Passage: [BOOK C:V–V]
Title:  [SERMON TITLE]
Preacher:  [PREACHER NAME]
Series:  [SERIES NAME]
Aired:  [DAY, DATE at TIME]
```

### Boilerplate

Reproduce this block verbatim at the end of every description:

```
Metro Church exists with the hope to "renew, retrain, and rebuild" the surrounding areas of Philadelphia, PA—through Christ-centered worship, genuine community, incarnational ministry, and radical generosity. To learn more about Metro, please visit us at https://metrophilly.org.

Stay connected with us:
Website » https://metrophilly.org
Facebook » https://www.facebook.com/metroeastfalls
Instagram » https://www.instagram.com/metroeastfalls
Youtube » https://mtro.cc/youtube
X » https://x.com/metroeastfalls
```

## Title options

When asked for titles (or proactively offer after delivering the description), generate 5–7 options in this format:

```
[Hook statement or question] ([Passage] — Sermon)
```

**Examples:**
- Why Jesus' Authority Changes Everything About Our Lives (Matthew 28:16–20 — Sermon)
- Where Sin Really Comes From and How God Answers It (Genesis 3:7–24 — Sermon)
- Why Grace Makes Some of Us Angry (Jonah 4:1–11 — Sermon)

Draw the hook from the sermon's central question or its most vivid, specific image — never generic. Give a spread: some optimized for search (phrasing a real person would type, e.g. "where does sin come from"), some for a stronger curiosity hook. Briefly note which is strongest for SEO vs. click appeal, and offer to generate more in a chosen direction.

## Working with the transcript

Transcripts are usually auto-generated, so expect artifacts: run-on sentences, mis-transcribed words, filler, "excuse me" self-corrections, odd capitalization of "bible," and mangled scripture wording. Read past these to the substance. Don't reproduce transcription errors, and don't treat a garbled scripture quote as the actual verse — reference it cleanly per NIV 1984.

## Quick workflow

1. Read the transcript; identify the passage, the sermon's explicit structure/points, the key images the pastor used, and the gospel turn.
2. Draft the three-paragraph body: hook → the sermon's actual movement → invitation to watch.
3. Append the metadata block (passage filled, rest as placeholders) and the verbatim boilerplate.
4. Deliver it copy-ready, then ask for title/preacher/series/air date and offer title options.
