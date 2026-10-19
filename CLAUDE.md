# Claude Code — Personal Memory Repo

At the start of every session in this repo, read the following files in order to restore context:

1. `profile.md` — stable facts about the user
2. `memories/current.md` — recent activity and active state
3. Any `projects/<slug>/overview.md` files relevant to what the user is working on

Do not invent or assume facts not present in these files. If a file is empty or stub-only, note
that to the user and ask if they want to populate it.

## Sync instructions

- Automated daily sync: `DAILY_SYNC_PROMPT.md`, run by the scheduled task "Claude memory —
  daily sync" at 05:45 Europe/London. Follow it when asked to "run the daily sync".
- Manual, interactive sync: `SYNC_PROMPT.md`. Follow it when the user asks to sync or update
  their memory by hand.

Raw transcripts are archived in Google Drive (`Claude/Transcripts-archive/`), never in this
repo. This repo holds summaries only; see "What never goes into GitHub" in
`DAILY_SYNC_PROMPT.md`.

## Branch

`claude/setup-memory-sync-rE9mG` is the default branch. Always commit and push to it.
