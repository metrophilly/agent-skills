# metrophilly/agent-skills

Shared Claude skills for Metro Church. Source of truth for the skills our team
uses in Claude Code and Claude.ai.

Distributed as a Claude Code plugin marketplace. The marketplace name is
`metrophilly`; the repo is `agent-skills`. They differ on purpose — see
[CONTRIBUTING.md](CONTRIBUTING.md).

## Install (Claude Code)

```
/plugin marketplace add metrophilly/agent-skills
/plugin install metro-sermon-content@metrophilly
/plugin install metro-engineering@metrophilly
```

Install only what you need. Content and comms people want
`metro-sermon-content`. Engineers want `metro-engineering`.

Skills from a plugin are namespaced by the plugin name:

```
/metro-sermon-content:metro-sermon-description
/metro-engineering:grill-me
```

The bare name (`/grill-me`) will not resolve.

Update later with:

```
/plugin marketplace update metrophilly
```

## Install (Claude.ai)

Skills here are plain folders. Download the skill directory and upload it in
Claude.ai settings. No plugin machinery required.

## Plugins

### metro-sermon-content

| Skill | Does |
| --- | --- |
| `metro-sermon-description` | Transcript to YouTube/Instagram video description in Metro's house format |
| `metro-sermon-titles` | 5–7 title options with SEO and click-appeal notes |

House style is enforced inside the skills: no em dashes anywhere in Metro
sermon copy, en dashes for passage ranges only, NIV 1984 default, hooks drawn
only from what the pastor actually preached.

### metro-engineering

| Skill | Does |
| --- | --- |
| `grill-me` | Interviews you on a plan or design until the decision tree is resolved |
| `ubiquitous-language` | Extracts a DDD glossary from a conversation into `UBIQUITOUS_LANGUAGE.md` |
| `improve-codebase-architecture` | Surfaces deepening opportunities and refactor candidates |

> `improve-codebase-architecture` is **incomplete**. Its `SKILL.md` links to
> `LANGUAGE.md`, `DEEPENING.md`, `INTERFACE-DESIGN.md`, and `HTML-REPORT.md`,
> which are stubs in this repo. Port the real content before the team relies
> on it.

## Auto-enable for a project

To have Claude Code register this marketplace for anyone who trusts a repo,
add to that repo's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "metrophilly": {
      "source": { "source": "github", "repo": "metrophilly/agent-skills" }
    }
  },
  "enabledPlugins": {
    "metro-engineering@metrophilly": true
  }
}
```

## Validate

```
claude plugin validate .
claude plugin validate ./plugins/metro-engineering
```

The first checks `marketplace.json`. The second checks a plugin's manifest and
its skill frontmatter — the marketplace-level run does not open skill files.
