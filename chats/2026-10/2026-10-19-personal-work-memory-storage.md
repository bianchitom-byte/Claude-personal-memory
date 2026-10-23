# Setting up the Claude memory sync

- **Dates:** 2026-10-19 → 2026-10-23
- **Source:** Claude Code (desktop app, this repo)
- **Transcript:** [Google Drive](https://drive.google.com/file/d/1EU5ZcTGSxxN8lLeWekDYTAPHPWs4WOPH/view)

## Asked
- Is anything continuously saving a memory of Claude work to GitHub or Notion? (No.) Then: set up a daily backup of Claude Code, claude.ai and Cowork sessions.

## Decisions
- **GitHub = summaries only.** Raw transcripts are kept out of git because of sensitive content and permanent history.
- **Raw archive = Google Drive** `Claude/Transcripts-archive/YYYY-MM/` (cleaned: Tom + Claude text, tool calls condensed, secrets redacted).
- **Offline copy = BIA-NAS**, weekly from the Mac mini.
- PTC and Schneider deal work appears in GitHub as one-liners only.
- Fixed branch: `claude/setup-memory-sync-rE9mG` (the repo's default; there is no `main`).
- claude.ai/Cowork chats are collected via Notion Memory (they can't be read directly); Tom to add a profile preference asking Claude to save summaries there.

## Outcome
- `DAILY_SYNC_PROMPT.md`, `sync-state.json` and the scheduled task "Claude memory — daily sync" (05:45 UK) created.
- First scheduled run (2026-10-23) failed: its session had no access to this repo (push 403) and no session-listing tools.
- Test sync run by hand on 2026-10-23 instead, covering sessions since 2026-10-18.

## Open threads
- Tom to add this repo as a source and the Claude Code Remote connector to the scheduled task.
- Tom to add the Notion Memory preference in claude.ai.
- Backfill of September sessions (Jarvis voice service, Notion Life OS integration, early Life-OS agent testing) not done.
