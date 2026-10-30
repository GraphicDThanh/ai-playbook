# weekly-digest-schedule

- **Skill:** [weekly-digest](../skills/weekly-digest/SKILL.md) @ 0.1.2
- **Platform:** TBD
- **Schedule:** TBD (cron + timezone)
- **Model:** TBD

## Prompt wrapper

```
Run the "weekly-digest" skill with:
- MODE: SCHEDULED
- WINDOW: previous Monday 00:00 → Sunday 23:59 (UTC+7)
- PUBLISH: yes
- DRY_RUN: false

This is an unattended scheduled run. No one will answer questions: do not ask for approval or clarification. Follow the skill exactly. Publish automatically, then return the OUTPUT report exactly as the skill defines it.
If the skill cannot be loaded, stop and report FAILED: "skill not loaded" — do not improvise a digest without it.
```

## How to test

TODO: manual run steps, compare output with `skills/weekly-digest/examples/`.
