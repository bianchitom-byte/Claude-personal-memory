# Claude Personal Memory

A portable, version-controlled record of Claude usage — enabling continuity across sessions, instances, and AI tools.

## Purpose

This repo preserves context so any Claude instance (or other AI) can pick up where the last one left off. Paste relevant files into a new chat to restore context instantly.

## Structure

```
/
├── README.md                    # This file
├── profile.md                   # Stable personal context ("who I am")
├── memories/
│   ├── current.md               # Active rolling memory snapshot
│   └── archive/YYYY-MM-DD.md    # Dated historical snapshots
├── projects/
│   └── <project-slug>/
│       ├── overview.md          # Goals, status, key decisions
│       ├── context.md           # Background a new Claude would need
│       └── artifacts/           # Code, docs, outputs worth keeping
├── chats/
│   └── YYYY-MM/<topic-slug>.md  # Distilled summaries of notable chats
└── CHANGELOG.md                 # What changed in each sync run
```

## How to use

### Starting a new Claude session with context

1. Open `profile.md` and paste it into the new chat.
2. If working on a specific project, also paste `projects/<slug>/overview.md` and `projects/<slug>/context.md`.
3. For recent activity, paste `memories/current.md`.

### Automatic daily sync

A scheduled task runs `DAILY_SYNC_PROMPT.md` every day at 05:45 UK time. It:
- summarises every Claude Code session and scheduled-task run from the past day into `chats/`
- pulls claude.ai and Cowork summaries saved to Notion Memory
- saves a cleaned raw transcript of each session to Google Drive, `Claude/Transcripts-archive/`
- updates `memories/current.md`, project overviews and `CHANGELOG.md`, then pushes

A weekly job on the Mac mini copies the Drive archive and this repo to BIA-NAS
(`/Volumes/Archive/Claude-backup/`).

### Syncing by hand

Run `SYNC_PROMPT.md` in Claude Code (web or CLI). Claude will:
1. Ask what's new since the last sync.
2. Update `memories/current.md` (archiving the previous version).
3. Update any relevant project files.
4. Commit the changes.

### Files to paste for maximum context

| Goal | Files to paste |
|------|---------------|
| General chat | `profile.md` + `memories/current.md` |
| Project work | above + `projects/<slug>/overview.md` + `projects/<slug>/context.md` |
| Full context | all of the above + relevant `chats/` entries |

## Conventions

- ISO dates (YYYY-MM-DD) everywhere.
- Plain markdown only — no HTML, no platform-specific syntax.
- Every file is self-contained: it should make sense pasted alone into a fresh chat.
- Bullet points over prose for scannability.
- `profile.md` and `memories/current.md` stay under ~500 lines each.

## Last synced

2026-05-13
