# User Template Schema

> **Created:** 2026-04-29 · **Updated:** 2026-05-04 (multi-zone restructure)
> **Purpose:** Schema for the per-user profile structure. Used for both real users (`users/[firstname-lastname]/`) and persona test runs.

---

## How to use

1. **Copy this entire directory** into the destination user folder:
   ```
   cp -r users/.template/* users/[firstname-lastname]/
   ```
2. **Delete every `README.md`** from the copied destination — those are template-only documentation, not data files.
3. **Populate** profile pages by filling in `[bracketed placeholders]` from the just-completed session content.
4. **Add the actual session-dated subdirectories** to `raw/` (e.g., `raw/s01-2026-05-15/transcript.md` + `feedback.md`) and the matching session file to `minutes/` (e.g., `minutes/s01-2026-05-15.md`).
5. **Append initial entries** to every change log file (`changes/profiles/[page].md` and `changes/artifact.md`).

---

## Directory structure

```
users/[firstname-lastname]/
├── artifact.md                   ← single deliverable, evolves across sessions
├── profiles/                     ← active profile pages (current state only)
│   ├── quick-profile.md
│   ├── identity.md
│   ├── pattern.md
│   ├── language.md
│   ├── life-context.md
│   ├── runner-manual.md
│   └── system-issues.md
├── inactive-profiles/            ← retired profile pages (parking lot)
├── raw/                          ← per-session verbatim records
│   └── sNN-YYYY-MM-DD/
│       ├── transcript.md
│       └── feedback.md
├── minutes/                      ← per-session narrative synthesis
│   └── sNN-YYYY-MM-DD.md
└── changes/                      ← evolution history
    ├── artifact.md               ← change log for the artifact
    ├── profiles/                 ← one change log per active profile page
    │   ├── quick-profile.md
    │   ├── identity.md
    │   ├── pattern.md
    │   ├── language.md
    │   ├── life-context.md
    │   ├── runner-manual.md
    │   └── system-issues.md
    └── inactive-profiles/        ← change logs for retired profile pages
```

---

## Architectural rules

- **Profile pages stay current-state only.** No change-log sections embedded in profile pages. Evolution lives exclusively in `changes/`.
- **Artifact evolves in place.** No per-session artifact snapshots. The change log at `changes/artifact.md` preserves the narrative of how the artifact has shifted.
- **Profiles travel with their change log.** When moving a profile from `profiles/` to `inactive-profiles/` (or back), move the matching change log too.
- **Raw records are write-once.** Never edit a raw transcript or feedback after the session ends — it's the historical baseline.
