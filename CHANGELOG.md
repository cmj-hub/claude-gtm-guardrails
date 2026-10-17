# Changelog

## 0.1.0 — 2026-10-17

- First public MIT release.
- Instrument: read by default, ask before a write, deny what nothing takes back.
- Banned: no CRM write without a prompt.
- Scorer `skills/gtm-guardrails/scripts/score_guardrails.py` (stdlib only): refuses whole-server and write-tool allow rules, missing ask rules for writes, deletes and merges that are not denied, `bypassPermissions`, and approval cards with no before value, source or undo line. Takes `--settings` to score a real settings file.
- Templates: `crm-read-only.settings.json`, `approval-card.md`, and the managed-settings template.
- Bundled from jaymount.com resources, unchanged: the undo sheet, the checker ladder, the routine pre-flight, the managed-settings template, and `skill_link_scan.py`.
- Context file `references/guardrails-context.md`: ten rules, each with its public source.
- Worked example: one open settings file taken to a passing one.
