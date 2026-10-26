# Changelog

## 0.1.1 (2026-10-26)

- `skill_link_scan.py` labels each link from its parsed host and path (`urllib.parse.urlsplit`), not a substring or regex. A link to another site that mentions your repo in its query, a look-alike repo name, or a fake host in userinfo (`example.com@other-host`) is now an outside link. `--own` matches only github.com or raw.githubusercontent.com paths that start with owner/repo. Backslashes are read as `/` (as browsers do), and any link with userinfo is an outside link.

## 0.1.0 (2026-10-17)

- First public MIT release.
- Instrument: read by default, ask before a write, deny what nothing takes back.
- Banned: no CRM write without a prompt.
- Scorer `skills/gtm-guardrails/scripts/score_guardrails.py` (stdlib only): refuses whole-server, write-tool and write-matching glob allow rules (including unanchored `mcp__*` and `*`), any core write verb with no ask rule, any of delete/remove/merge not denied, `bypassPermissions`, and approval cards with no before value, source or undo line. Takes `--settings` to score a real settings file.
- Templates: `crm-read-only.settings.json`, `approval-card.md`, and the managed-settings template.
- Bundled from jaymount.com resources, unchanged: the undo sheet, the checker ladder, the routine pre-flight and the managed-settings template. `skill_link_scan.py` is bundled with one fix: CSV cells that start with `=`, `+`, `-`, `@`, tab or CR get a leading quote, so a spreadsheet cannot run them as formulas.
- Context file `references/guardrails-context.md`: ten rules, each with its public source.
- Worked example: one open settings file taken to a passing one.
