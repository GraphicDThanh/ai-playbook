# ai-playbook

Registry of skills and schedules. Skill = portable core. Schedule = where/when it runs.

## Skills

| Skill | Version | Path |
|-------|---------|------|
| ai-dev-digest | 0.1.0 | [skills/ai-dev-digest](skills/ai-dev-digest/SKILL.md) |

## Schedules

| Schedule | Skill | Platform | Cron | Model |
|----------|-------|----------|------|-------|
| ai-dev-digest-weekly | ai-dev-digest | TBD | TBD | TBD |

See [schedules/ai-dev-digest-weekly.md](schedules/ai-dev-digest-weekly.md).

## Layout

- `skills/<name>/SKILL.md` — core, portable. `CHANGELOG.md` for versions. `examples/` good sample outputs for comparison.
- `schedules/<name>.md` — platform, cron, model, prompt wrapper, how to test.
- `evals/<name>/` — added later when needed.
