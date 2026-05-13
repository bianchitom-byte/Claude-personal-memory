# Claude Personal Memory Sync

You are maintaining a portable, version-controlled record of my Claude usage so I can move
context between Claude instances (or other AI tools) without losing continuity.

## Repository structure

```
/
├── README.md                    # Overview + how to use this repo
├── profile.md                   # Stable personal context (the "who I am" file)
├── memories/
│   ├── current.md               # Active rolling memory snapshot
│   └── archive/YYYY-MM-DD.md    # Dated snapshots for history
├── projects/
│   └── <project-slug>/          # Lowercase-hyphenated (e.g. financial-planning)
│       ├── overview.md          # Goals, status, key decisions
│       ├── context.md           # Background a new Claude would need
│       └── artifacts/           # Code, docs, outputs worth keeping
│           └── .gitkeep
├── chats/
│   └── YYYY-MM/<topic-slug>.md  # Distilled summaries of notable chats
└── CHANGELOG.md                 # What changed in each sync run
```

## On every run

1. Read README.md, CHANGELOG.md, and memories/current.md to understand prior state.
   Also read the header section of profile.md for stable identity context.

2. Ask me in one batch:
   - Any new memories/context to add since last sync
   - Any new or updated projects to record
   - Any notable chats from other Claude instances to summarise
   - Any artifacts to save

   If my answers are incomplete, ask one follow-up round before proceeding with
   what's available.

3. If I report nothing has changed, make no file writes and no commit.
   Acknowledge the run as a no-op and stop.

4. For each project, ensure overview.md ends with "Last updated: <date>"
   and a "Status" line (active / paused / archived).

5. Update memories/current.md to reflect the latest stable state.
   Archive the previous current.md to memories/archive/<snapshot-date>.md,
   where <snapshot-date> is the "Snapshot date" field from inside the old current.md.

6. Keep profile.md updated only when stable facts change (location, family, long-term
   preferences). Do not put transient project state here.

7. Append a dated entry to CHANGELOG.md describing what changed.

8. Stage and commit all changes in a single commit:
   "sync: <date> — <one-line summary>"
   Then push to the remote branch.

## Formatting rules

- Plain markdown only. No HTML, no Notion-specific syntax.
- Every file must be self-contained: pasting it into a fresh Claude chat gives useful context
  with no other files required.
- Use ISO dates (YYYY-MM-DD) everywhere.
- Prefer bullet points over prose for scannable context.
- profile.md and memories/current.md: max ~500 lines each. Split if larger.

## First run

If the repo is empty:
1. Scaffold the full structure above. Add a .gitkeep file in every artifacts/ directory.
2. Write a README explaining the system.
3. Create stub files for profile.md and memories/current.md.
4. Commit and push the scaffold: "sync: <date> — initial scaffold"
5. Ask me to populate profile.md with my core context. Do not invent facts about me.
