# Current Memory Snapshot

> Rolling summary of active context. Paste into a new Claude session to restore recent state.
> Updated each sync run; previous version archived to `memories/archive/`.

**Snapshot date:** 2026-11-26
**Previous snapshot:** 2026-10-23 (`memories/archive/2026-10-23.md`)

## Recent Activity

- 2026-11-24: gathered 2025/26 Self Assessment documents for accountant Andy (The Tax Hive); several gaps remain. ([summary](../chats/2026-11/2026-11-24-tax-return-pack-for-andy.md))
- 2026-10-18–20: finished migrating the WD MyBook to BIA-NAS; WD decommissioned 2026-10-19. ([summary](../chats/2026-10/2026-10-19-nas-migration-status-check.md))
- 2026-10-18: asked about a native Xbox Cloud Gaming client for macOS; Greenlight recommended. ([summary](../chats/2026-10/2026-10-18-native-xbox-live-app-for-macos.md))
- 2026-10-19–23: set up the automated Claude memory sync (GitHub summaries, Drive transcripts, weekly NAS copy). ([summary](../chats/2026-10/2026-10-19-personal-work-memory-storage.md))
- 2026-10-23: Life OS status check — Jarvis down (CLI login expired), Notion integration only half built. ([summary](../chats/2026-10/2026-10-23-life-os-agent-testing-issue.md))
- Ongoing scheduled work: Schneider–PTC deal watch and Schneider/AVEVA research tasks; LinkedIn weekly drafts; chief-of-staff briefs.

## Active Projects

- **Life OS / Jarvis** (`projects/personal-life-admin/`): chief-of-staff agent on the Mac mini plus Notion Life OS store.
- **Home IT / NAS** (`projects/smart-home/`): BIA-NAS is the only NAS; weekly Claude backup lands there.
- **Claude memory sync** (this repo): daily scheduled task, Drive archive, NAS copy.

## Open Threads / Decisions Pending

- **2025/26 tax return:** download iCloud placeholders on the Mac; still need E*Trade gains/losses and vest confirmations, 25/26 bank interest, payments on account, Emma's P60 and UTR; upload via Andy's portal.
- **Jarvis or cloud?** Tom to pick which chief-of-staff system is live; first run `claude auth login` on the Mac mini.
- Jarvis launchd schedule fix waiting on Tom (remove git lock file, reload jobs).
- Memory sync task needs this repo added as a source and the Claude Code Remote connector, in the scheduled task's settings.
- Add the Notion Memory preference in claude.ai so claude.ai/Cowork chats get collected.
- Backfill September sessions into the archive.
- NAS tidy-up (UGOS update, failed jobs, hidden temp file); investigate NAS shutdown and Mac mini drive drop-outs.

## Things Claude Should Remember Right Now

- When a background job stalls on something only Tom can fix, alert him straight away rather than waiting.
- GitHub gets summaries only; PTC/Schneider deal work is one line per item.
- `profile.md` is still an empty template.

## Notes for Next Sync

- Session-listing tools have been missing since late October; Claude Code sessions from 2026-10-23 onwards are not yet archived. Re-run once the Claude Code Remote connector is available.

- Update the "Personal work memory storage" Drive transcript (session still open on 2026-10-23).
