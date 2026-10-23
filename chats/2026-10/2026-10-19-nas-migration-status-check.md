# NAS migration: WD MyBook → BIA-NAS

- **Dates:** 2026-10-18 → 2026-10-20
- **Source:** Claude Code (Remote Control CLI on the Mac mini)
- **Transcript:** [Google Drive](https://drive.google.com/file/d/1RQ7zaqGP-T4_xoZ7VqmfCHShwrqjQ2ju/view)

## Asked
- Finish copying the WD MyBook Live shares (Public, OldBackup) to BIA-NAS `Archive`, verify, and say when the WD can be switched off.
- Set up a weekly NAS backup of the Claude memory archive (request from the memory-storage session).

## Outcome
- Copy completed and verified file by file (name + size); only differences were an empty 2014 `test.mp3` and 3 symlinks.
- TimeMachine and SmartWare shares on the WD declared out of scope by Tom.
- **WD MyBook decommissioned 2026-10-19.** BIA-NAS (UGREEN) is now the only NAS.
- Mac mini repeatedly lost its SMB mounts during the copy; NAS shut down abnormally once.
- Standing preference saved: when a background job stalls on something only Tom can fix, alert him straight away.
- Google Drive for Desktop installed on the Mac mini; `Transcripts-archive` set available offline.
- Weekly backup installed: `~/bin/claude-backup-to-nas.sh` + LaunchAgent `com.tom.claude-backup-to-nas`, **Sundays 03:00**, first run 2026-10-25. Copies the Drive `Transcripts-archive` folder and a git mirror of this repo to `Archive/Claude-backup/`. Additive only; skips if the NAS isn't mounted. Log: `~/Library/Logs/claude-backup-to-nas.log`. Tested twice by hand.

## Open threads
- Optional tidy-up: install UGOS update 1.20.0.0142; clear failed NAS copy jobs; delete a 1.09 GB hidden temp file in `Archive/Shared Videos/Movies`; remove the WD network folders from the NAS.
- Investigate the NAS abnormal shutdown and Mac mini drive drop-outs (power cable, UPS, Ethernet).
- Spun off a separate local session to fix the Jarvis launchd schedules (8h offset gone since the 3 Oct reboot); waiting on Tom to remove a git lock file and reload the jobs.
