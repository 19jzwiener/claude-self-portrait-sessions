# users/

> Where your multi-page profile lives after you complete a session.

When you finish Session 1, the Session Runner creates a directory here named after you (`firstname-lastname/`) containing 7 profile pages plus a per-session subdirectory. This is your structured self-portrait — the system uses it as context for any future sessions you run.

## Structure

```
users/
├── README.md                  (this file)
├── .template/                 (the schema — copied into your dir on first session)
└── firstname-lastname/        (your dir — created when you run Session 1)
    ├── quick-profile.md       (cheat-sheet of who you are right now)
    ├── identity.md            (Your Name + etymology + stickiness signal)
    ├── pattern.md             (your named leak + active commitment + WOOP)
    ├── language.md            (vocabulary you actually use)
    ├── life-context.md        (people / projects / places / body / time)
    ├── runner-manual.md       (calibration notes for future Session Runners)
    ├── system-issues.md       (where the session friction was, for you)
    └── sessions/
        └── s01-YYYY-MM-DD.md  (frozen record of Session 1)
```

## Privacy

Your `firstname-lastname/` directory is gitignored — it never gets pushed to GitHub by accident. The `.template/` directory and this README ARE tracked, since they're part of the shipped schema.

If you fork this repo or contribute back via PR, your personal profile won't be staged.
