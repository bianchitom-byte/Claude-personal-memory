# Claude Code — Personal Memory Repo

At the start of every session in this repo, read the following files in order to restore context:

1. `profile.md` — stable facts about the user
2. `memories/current.md` — recent activity and active state
3. Any `projects/<slug>/overview.md` files relevant to what the user is working on

Do not invent or assume facts not present in these files. If a file is empty or stub-only, note
that to the user and ask if they want to populate it.

## Sync instructions

The full sync prompt is in `SYNC_PROMPT.md`. Follow it when the user asks to sync or update
their memory.

## Branch

Development happens on `claude/setup-memory-sync-rE9mG`. Always commit and push to that branch.
