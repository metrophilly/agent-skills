---
name: metro-sermon-metadata
description: Fill in the sermon metadata block (passage, title, preacher, series, air date) for a Metro sermon video description. Use right after generating a Metro sermon description or titles when preacher, series or air date are still placeholders, or when the user says "fill in the metadata", "what series is this", "set the air date", or "finish the description". Also use when a transcript file name carries a date, and when a spoken passage may differ from the scripture file.
---

# Metro sermon metadata

Every description leaves preacher, series and air date as placeholders. This skill closes them in one pass, with one question at most.

## Resolve each field

Passage. Take it from the transcript, where the reader almost always states it. If a scripture file is also supplied, compare the two. Report any mismatch, such as a spoken chapter that differs from the text read. Use an en dash for ranges. Default translation is NIV 1984.

Air date. Read it from the file name when it carries one, for example a name ending in "4oct" gives October 4. Take the year from today's date and say which year you used. Sunday services are the norm, so flag a date that is not a Sunday. Never invent a service time. Ask for it or leave it blank.

Preacher. Use a name only when the transcript names or introduces the speaker. Never fill it from your general knowledge of who usually preaches. A guess in a public description is worse than a blank.

Series. Read `references/series.md`. If the passage book or theme matches a row, propose that series and confirm it. If nothing matches, ask.

Title. Use the title the user chose. If none was chosen, leave the placeholder and offer title options through the metro-sermon-titles skill.

## Ask once

List every field still open in one short question. Do not ask field by field. Do not ask for a field you resolved. When the user answers, return the completed metadata block, copy-ready, in the same format as the description skill.

## Keep the registry current

When the user names a series that is not in `references/series.md`, give them one line to add to that file. The registry is edited by pull request.

## House rules

No em dashes, except the one in the fixed description boilerplate, which stays as written. En dashes for passage ranges only. Placeholders stay in square brackets until a source supplies the value.
