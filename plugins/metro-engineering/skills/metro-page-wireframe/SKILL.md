---
name: metro-page-wireframe
description: Build hi-fi wireframes and page mockups for metrophilly.org in Metro's real design system, with real site assets. Use whenever the user asks for a wireframe, mockup, layout, "hi-fi", new page section, or redesign of a Metro page (Advance, Advent, Cherry Hill, Events, history, RE:NEW, campus pages, homepage), or says "wireframe this page", "what could this page look like", or "mock up these sections". Trigger even when the user only lists sections and never says "wireframe".
---

# Metro page wireframe

Produce a page the reviewer can click through and judge as if it were the live site. A wireframe in Metro's real tokens, real photos and real components lets the reviewer react to the design, not to the placeholders.

## Before you draw

Get the site repo (read access, shallow clone) and read three things first.

1. The token source, `styles/globals.css`, in the Tailwind CSS v4 `@theme` block. Use the compiled values. Some documented tokens use Tailwind v3 names that do not compile under v4, so a documented 64px can render as 60px. When docs and the theme block disagree, the theme block wins.
2. The existing component for each section type, for example the hero component with video. Reuse its structure and name it in your handoff so an engineer can map the wireframe to code.
3. The image library. Build contact sheets of the stock photos, leadership photos, campus panoramas, ministry photos, logos and graphics, then choose from what exists.

## Brand rules

Metro feels warm but clean, crisp, friendly but elevated. The palette is Moss green and Latte cream. Display type is EB Garamond. Body and UI type is Inter or Work Sans. Buttons use an 8px radius. Set text in brand tokens. Do not fall back to the Tailwind default grey, which is what most live text renders in today and is a known gap.

Default the hero to a full-screen looping video, as on the live site, unless the user asks for something else.

Brand rules override any outside style source. If you borrow patterns from reference design systems, take structure and interaction only. If you use a general style skill, list its defaults that conflict with Metro and override them. A past run with an external style skill produced torn paper and receipt effects that the user rejected as cartoonish and off brand.

## Build rules

Fill every image slot with a real asset from the repo. Use a labeled placeholder only when no fitting asset exists. Do not use an asset that does not fit the topic, for example a business book cover on a giving page.

Build the interactions the page needs, such as a step walkthrough, a calculator or a filterable grid. The reviewer judges by clicking.

Never write testimonials, statistics or giving instructions that look real. Mark invented content as placeholder. Flag these gaps in your reply: photos paired with quotes that need the member's consent, missing real screenshots of the giving platform, and any copy a pastor must approve.

Public copy on the page follows the metro-copy-voice skill when it is installed. Never put a minor's full name or grade on a public page.

Check the page at desktop and phone width before you send it.

## Versions and feedback

Keep each version as its own named board on one canvas, for example v1, v2, v3. Do not overwrite earlier versions, so the user can compare and say "stick with v2". Overwrite only when the user asks. If the session offers a Design artifact type, use it.

The user gives short, direct feedback. When a version is called bad, too playful or off brand, ask one or two targeted questions about what drifted, then correct. Do not re-explain the design.

## Handoff

End with a short note: which tokens and components the page uses, which repo assets it uses, and the open gaps. One sentence on the outcome. No recap of the steps.
