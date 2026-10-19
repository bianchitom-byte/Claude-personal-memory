# Changelog

All sync runs are recorded here in reverse-chronological order.

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
