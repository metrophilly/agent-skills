# metro-sermon-content

Sermon video copy in Metro's house style.

```
/plugin install metro-sermon-content@metrophilly
```

| Skill | Invoke |
| --- | --- |
| Video description from a transcript | `/metro-sermon-content:metro-sermon-description` |
| Title options | `/metro-sermon-content:metro-sermon-titles` |
| Preacher, series and air date for the metadata block | `/metro-sermon-content:metro-sermon-metadata` |
| Three-level small group questions | `/metro-sermon-content:metro-sermon-discussion-questions` |
| Series tagline and card subtitle | `/metro-sermon-content:metro-sermon-series-tagline` |
| Metro's two writing registers and shared copy rules | `/metro-sermon-content:metro-copy-voice` |
| Reformed, confessional lens for Bible and theology questions | `/metro-sermon-content:reformed-research` |

The skills usually trigger on their own — paste a transcript and ask for a
description and the skill loads without the slash command.

Non-negotiables encoded in the skills: only what the pastor actually preached,
no em dashes in any Metro sermon copy, en dashes for passage ranges only,
NIV 1984 as the default translation.

`reformed-research` sets a confessional Reformed lens as the default for every
Bible or theology question in a session. Install this plugin only if that is
the lens you want.

`metro-sermon-metadata` reads `references/series.md`. Add a row there by pull
request when a new series starts.
