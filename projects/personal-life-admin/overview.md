# Personal Life Admin Assistant

## Goals

- Run a chief-of-staff agent ("Jarvis") for household, travel, home programme and money admin, with Notion Life OS as the shared store.

## Status

active

## Key Decisions

- Permission register governs what the agent may do; fail closed if it can't be read.
- Open items tracked as `OI-nn` in Notion and the Life-OS repo.

## Current Focus

- Deciding whether Jarvis (Mac mini, Life-OS repo) or the older cloud scheduled tasks are the live system.

## Open Questions / Next Steps

- Jarvis down since 2026-10-23 07:00: run `claude auth login` on the Mac mini.
- Pick "Jarvis" or "cloud"; then merge OI-34..47 into the repo and retire the duplicate system.
- Jarvis launchd schedule fix awaiting git lock removal and job reload.
- See `chats/2026-10/2026-10-23-life-os-agent-testing-issue.md`.

---

Last updated: 2026-10-23
