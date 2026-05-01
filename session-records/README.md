# session-records/

> Where each session's run records live (transcript + feedback + shareable artifact).

When you finish Session 1, the Session Runner creates a per-run directory here named `YYYY-MM-DD-firstname-lastname/` containing the session's outputs.

## Structure

```
session-records/
├── README.md                              (this file)
└── YYYY-MM-DD-firstname-lastname/         (one per session run)
    ├── transcript.md     (every screen's verbatim user input + the final artifact)
    ├── feedback.md       (post-session Mom Test Q&A)
    ├── artifact.html     (shareable HTML version of your profile)
    ├── artifact.md       (markdown version, optional)
    └── artifact.txt      (plain-text version, optional)
```

## Why per-run dirs?

Each time you run a session — Session 1 today, Session 2 next week, Session 3 next month — its records get their own date-prefixed directory. This keeps each session's record self-contained while letting your `users/firstname-lastname/` profile compound across runs.

## Privacy

Per-run dirs are gitignored — never pushed by accident. The README is tracked.
