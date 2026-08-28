# Contributing

## Adding a skill to an existing plugin

1. `mkdir plugins/<plugin>/skills/<skill-name>`
2. Write `SKILL.md` with frontmatter:

```markdown
---
name: your-skill-name
description: What it does, then when to use it. Include the literal phrases a user would say.
---
```

3. `claude plugin validate ./plugins/<plugin>`
4. Test locally: `/plugin marketplace add ./` from a checkout, install, invoke.
5. PR.

Nothing to register — plugins scan their `skills/` directory automatically.

## Writing the description field

This is the only part Claude reads when deciding whether to load the skill.
Everything else is invisible until it triggers. Write it as *what it does* plus
*when to use it*, and include the actual words someone would type. Compare:

- Weak: `Helps with sermon copy.`
- Strong: `Generate a YouTube description for a Metro sermon from a raw transcript. Use when the user pastes a transcript and asks for a "YouTube description," "video description," or "sermon description."`

If a skill isn't firing, the description is almost always the reason.

## Adding a new plugin

1. `plugins/<name>/.claude-plugin/plugin.json` — see an existing one
2. Add an entry to `.claude-plugin/marketplace.json` with `"source": "./plugins/<name>"`
3. `claude plugin validate .`

Group by audience, not by topic. A plugin is what one person installs in one
command. Five plugins of one skill each means five install commands and nobody
runs all five.

## Naming

- Skill and plugin names: kebab-case, lowercase, digits and hyphens only.
- Marketplace name stays `metrophilly`. It does **not** match the repo name.
  `agent-skills` is on Claude Code's reserved-marketplace-name list and a
  marketplace using it stops loading. The repo name is unaffected.
- A plugin `name` is its stable identifier — users have it in their settings.
  To change the label shown in the UI, add `displayName` and leave `name` alone.
  If you truly must rename, add a `renames` entry in `marketplace.json` mapping
  old name to new, or to `null` if removed, so existing installs migrate.

## Versioning

Do not add a `version` field to `plugin.json` or to marketplace entries.

For git-based sources, omitting it makes Claude Code use the resolved commit
SHA, so merging to `main` is the release. Setting it pins the plugin until
someone remembers to bump the string, and a stale value means volunteers
silently run old skills. If we ever need release channels, we add versions
deliberately, not by accident.

## Don't

- No top-level `bin/` in a plugin. Put executables in `scripts/` and reference
  them as `${CLAUDE_PLUGIN_ROOT}/scripts/<name>`.
- No `../` paths. Plugins are copied to a cache on install, so anything outside
  the plugin directory won't be there. Symlink if you need to share.
- No credentials, internal hostnames, or private URLs. This repo is public.
