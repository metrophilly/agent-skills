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
| `metro-sermon-metadata` | Fills preacher, series and air date in one pass |
| `metro-sermon-discussion-questions` | Three-level small group questions from a sermon |
| `metro-sermon-series-tagline` | One-sentence series tagline and card subtitle |
| `metro-copy-voice` | Internal and public writing registers, plus shared copy rules |
| `reformed-research` | Reformed, confessional default lens for Bible and theology questions |

House style is enforced inside the skills: en dashes for passage ranges, an em
dash between the passage and "Sermon" in the title format (the only em dash in
Metro sermon copy, aside from the one inside the fixed boilerplate), NIV 1984
default, hooks drawn only from what the pastor actually preached.

### metro-engineering

| Skill | Does |
| --- | --- |
| `grill-me` | Interviews you on a plan or design until the decision tree is resolved |
| `ubiquitous-language` | Extracts a DDD glossary from a conversation into `UBIQUITOUS_LANGUAGE.md` |
| `improve-codebase-architecture` | Surfaces deepening opportunities and refactor candidates |
| `metro-page-wireframe` | Hi-fi page wireframes in Metro's real tokens and assets |
| `expert-audit` | Audits from raw data with named methods and outside validation |

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
