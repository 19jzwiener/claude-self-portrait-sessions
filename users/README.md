# users/

> Where your multi-page profile lives after you complete a session.

When you finish Session 1, the Session Runner creates a directory here named after you (`firstname-lastname/`). It contains your evolving artifact, structured profile pages, raw session records, narrative minutes, and a change log per dimension. This is your structured self-portrait — the system uses it as context for any future sessions you run, and the artifact (the one-page profile) is yours to share or revisit.

## Structure

```
users/
├── README.md                         (this file)
├── .template/                        (the schema — copied into your dir on first session)
└── firstname-lastname/               (your dir — created when you run Session 1)
    ├── artifact.md                   (your current one-page profile, evolves across sessions)
    ├── profiles/                     (system-internal profile pages — current state)
    │   ├── quick-profile.md
    │   ├── identity.md
    │   ├── pattern.md
    │   ├── language.md
    │   ├── life-context.md
    │   ├── runner-manual.md
    │   └── system-issues.md
    ├── inactive-profiles/            (parking lot for dimensions you've retired)
    ├── raw/                          (verbatim records of each session)
    │   └── sNN-YYYY-MM-DD/
    │       ├── transcript.md
    │       └── feedback.md
    ├── minutes/                      (per-session narrative synthesis)
    │   └── sNN-YYYY-MM-DD.md
    └── changes/                      (evolution history per page + artifact)
        ├── artifact.md
        ├── profiles/                 (one log per active page)
        └── inactive-profiles/        (logs for retired pages)
```

## Privacy

Your `firstname-lastname/` directory is gitignored — it never gets pushed to GitHub by accident. The `.template/` directory and this README ARE tracked, since they're part of the shipped schema.

If you fork this repo or contribute back via PR, your personal profile won't be staged.

## What gets kept

The system stores raw session records (transcripts + feedback), narrative minutes, current-state profile pages, the evolving artifact, and per-page change logs. All of it stays on your machine. None of it is shared, sold, mined, or rummaged through. The point of keeping it is so future sessions can compound on what you already said — the system's goal is to know who you are *today*, not to surveil who you used to be.
