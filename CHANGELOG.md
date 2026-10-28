# Changelog

All sync runs are recorded here in reverse-chronological order.

---

## 2026-10-23 — Daily sync (manual test run, 4 sessions)

- Scheduled run at 04:46 UTC failed: no repo access (push 403) and no session-listing tools.
- Ran the sync by hand from the setup session, window 2026-10-18 → 2026-10-23.
- Sessions: Xbox app for macOS; NAS migration; Life OS / Jarvis status; memory sync setup.
- 4 cleaned transcripts uploaded to Drive `Claude/Transcripts-archive/2026-10/`.
- Summaries in `chats/2026-10/`; scheduled-task runs logged as one-liners.
- `memories/current.md` rewritten (old snapshot archived to `memories/archive/2026-05-13.md`);
  `personal-life-admin` and `smart-home` overviews filled in.
- Notion Memory empty: no claude.ai/Cowork summaries yet.
- Not done: September sessions (backfill listed in `sync-state.json`).
- `DAILY_SYNC_PROMPT.md`: paging by inner timestamp, condensed tool lines, scheduled runs as one-liners.

---

## 2026-10-19 — Automated daily sync

- Added `DAILY_SYNC_PROMPT.md` and `sync-state.json` for a daily scheduled sync at 05:45 UK.
- Raw transcripts go to Google Drive `Claude/Transcripts-archive/`; GitHub keeps summaries only.
- claude.ai and Cowork chats are collected via Notion Memory.
- Weekly NAS copy to BIA-NAS `/Volumes/Archive/Claude-backup/` from the Mac mini.
- Added `chats/` and `memories/archive/` directories; updated `CLAUDE.md` and `README.md`.

---

## 2026-05-13 — Prompt optimisation & repo fixes

- Added `SYNC_PROMPT.md` with optimised sync prompt (8 issues fixed vs original).
- Added `.gitkeep` to all `artifacts/` directories so they persist in git.
- Key prompt changes: always push on completion; read `memories/current.md` on startup;
  archive naming uses snapshot date field; no-op run guidance; slug convention specified;
  first-run now commits before asking for content; follow-up round allowed on partial answers.

---

## 2026-05-13 — Initial scaffold

- Created repo structure: `README.md`, `profile.md`, `memories/`, `projects/`, `chats/`, `CHANGELOG.md`.
- Created stub `profile.md` (awaiting user population).
- Created initial `memories/current.md`.
- No projects or chats recorded yet.

## 2026-10-23 — daily sync (partial, no sessions processed)

- Session-listing tools (`list_sessions`, `list_events`, `list_triggers`) were not available in this session (Claude Code Remote connector not attached), so Claude Code sessions and scheduled-task runs could not be read.
- Notion Memory was reachable but empty (no entries).
- No Drive or summary files written. `last_run_utc` left unchanged.
- Fix: add the Claude Code Remote connector to the "Claude memory — daily sync" task's settings.

## 2026-10-24 — daily sync (partial, no sessions processed)

- Same gap as 2026-10-23: `list_sessions`, `list_events` and `list_triggers` were not available (Claude Code Remote connector tools not exposed), so Claude Code sessions and scheduled-task runs could not be read.
- Notion Memory was reachable but still empty.
- No Drive or summary files written. `last_run_utc` left unchanged.
- Fix still outstanding: attach the Claude Code Remote connector in the task's settings.

## 2026-10-25 — daily sync (partial, no sessions processed)

- Third consecutive run without `list_sessions`, `list_events` or `list_triggers` (Claude Code Remote connector tools not exposed), so Claude Code sessions and scheduled-task runs could not be read.
- Notion Memory reachable but still empty.
- No Drive or summary files written. `last_run_utc` left unchanged.
- Fix still outstanding: attach the Claude Code Remote connector in the task's settings.

## 2026-10-26 — daily sync (partial, no sessions processed)

- Fourth consecutive run without `list_sessions`, `list_events` or `list_triggers` (Claude Code Remote connector tools not exposed), so Claude Code sessions and scheduled-task runs could not be read.
- Notion Memory reachable but still empty.
- No Drive or summary files written. `last_run_utc` left unchanged.
- Fix still outstanding: attach the Claude Code Remote connector in the task's settings.

## 2026-10-27 — daily sync (partial, no sessions processed)

- Fifth consecutive run without `list_sessions`, `list_events` or `list_triggers` (Claude Code Remote connector tools not exposed), so Claude Code sessions and scheduled-task runs could not be read.
- Notion Memory reachable but still empty.
- No Drive or summary files written. `last_run_utc` left unchanged.
- Fix still outstanding: attach the Claude Code Remote connector in the task's settings.

## 2026-10-28 — daily sync (partial, no sessions processed)

- Sixth consecutive run without `list_sessions`, `list_events` or `list_triggers` (Claude Code Remote connector tools not exposed), so Claude Code sessions and scheduled-task runs could not be read.
- Notion Memory reachable but still empty.
- No Drive or summary files written. `last_run_utc` left unchanged.
- Fix still outstanding: attach the Claude Code Remote connector in the task's settings.
