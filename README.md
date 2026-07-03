# skill-check

Starter template for [ModelBound Skill Check](https://modelbound.co/connect/github-actions) in GitHub Actions.

[![ModelBound Skill Trust](https://modelbound.co/api/badge/skills.svg?repo=ModelBound/skill-check)](https://modelbound.co/connect/github-actions)
![Skill Lint](https://modelbound.co/api/badge/skills.svg?repo=ModelBound/skill-check&metric=lint)
![Optimize Savings](https://modelbound.co/api/badge/skills.svg?repo=ModelBound/skill-check&metric=optimize)

## Setup

1. Copy `.github/workflows/modelbound-skills.yml` into your repo.
2. Add a `MODELBOUND_API_KEY` secret (`mb_live_…` from [API Keys](https://modelbound.co/settings/api-keys)).
3. Commit skill files under paths matched by the default globs (`.modelbound/`, `.cursor/rules/`, `.claude/skills/`, etc.).

## Action repo

The reusable action lives at [ModelBound/skill-check-action](https://github.com/ModelBound/skill-check-action).

## Modes

| Mode | API key | What runs |
| --- | --- | --- |
| `lint` | No | Local SKILL.md lint via `modelbound-mcp` |
| `trust` | Yes | Lint + trust score |
| `optimize` | Yes | Lint + optimize dry-run estimate |
| `full` | Yes | Lint + trust + optimize + public badge report |

## Example skill layout

```
.github/skills/ci-smoke/SKILL.md
.cursor/rules/my-rule.mdc
.modelbound/my-skill.md
.claude/skills/review/SKILL.md
```
