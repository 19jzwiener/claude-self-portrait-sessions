# claude-self-portrait-sessions

> A 30-45 minute self-discovery session you run with Claude Code. Walk away with a multi-page profile of who you are right now — in your own words.

**Want more context first?** See the [Session 1 preview page](https://life-os-preview.netlify.app/session-1-preview.html) for what the session is + what you walk away with + how it fits into a longer journey.

## What this is

Six questions, around 30-45 minutes, with Claude as the session runner. You answer in your own words. Claude reads them back to you, helps you write your two sentences, names the pattern that throws you off, offers three directions you could take next, and ends with one observation that's hard to ignore.

You leave with a multi-page profile of yourself: Your Name (a 3-5 word handle for who you are right now), your two sentences, your named pattern, your next move (with a specific trigger so you actually do it), checkpoint dates, three open questions for next time, plus structured pages capturing the language you use, life context, and notes for future sessions.

**Who it's for:** Anyone who wants to say something true about themselves they've been half-knowing for a while — not a personality test, not coaching, not therapy. A structured self-portrait.

**Who it's not for:** People looking for a personality quiz, a productivity tool, or a generic life-coaching assistant. The methodology is direct and the negative surprise is meant to land.

## Quick Start (3 steps)

```bash
git clone https://github.com/19jzwiener/claude-self-portrait-sessions.git
cd claude-self-portrait-sessions/runtime/session-one
claude
```

That's it. Claude reads `CLAUDE.md`, becomes the Session Runner, and starts the session by asking your first name. Block 30-45 uninterrupted minutes.

> **Upgrading from v0.1.0?** As of v0.2.0 (2026-05-01), runtime files moved from the repo root into `runtime/session-one/`, and Session 1 was upgraded to V2 (multi-page profile output, "Your Name" framing, refined script). After `git pull`, `cd runtime/session-one` instead of the old root path.

## What you get

| Field | What it is |
|-------|------------|
| **Your Name** | A 3-5 word handle that captures both your strength and your tension. You confirm whether it lands; if it doesn't, write reasons it feels off (those carry into Session 2). |
| **Two Sentences** | Two of your own sentences: "I come alive when ___" and "I drift when ___". |
| **Pattern** | A named character (you name it) — what it does to you, and when it loses power. |
| **Vector** | One of three paths you can take, written as a concrete next step with a specific moment that triggers it. |
| **Negative Surprise** | One sentence using your own vocabulary, naming a pattern that's hard to see from the inside. |
| **Checkpoints** | Two real calendar dates for your next move. |
| **Three Gap Questions** | Open questions specific to your session, designed to compound into Session 2 if you come back. |

You also get a **multi-page profile** at `users/firstname-lastname/` containing structured pages for identity, pattern, language, life-context, runner-manual, and system-issues — these compound across future sessions.

See [`runtime/session-one/examples/sample-session-carlos.md`](runtime/session-one/examples/sample-session-carlos.md) for a complete walkthrough — a fictional 48-year-old construction foreman runs the session and walks away with "The Providing Stranger" as Your Name, "El Viejo" as his named pattern, and a Saturday-Rule first move. (Note: the sample shows the V1 single-page artifact format. V2 generates the multi-page profile in `users/`; see `users/.template/` for the V2 schema.)

## How it works

When you `cd` into `runtime/session-one/` and run `claude`, Claude reads `CLAUDE.md` (the Session Runner instructions) and starts running the script in `session-1-script.md`. The script is read verbatim — Claude doesn't paraphrase.

Four fields are generated live from your answers using the rules in `generation-rules.md`:
- The 3 vector options (after Phase A intake)
- The first move (after you pick a vector)
- The negative surprise
- Your Name + 3 gap questions

After the session ends, two things happen:
1. Your **transcript + feedback + shareable artifact** land in `session-records/YYYY-MM-DD-firstname-lastname/`
2. Your **multi-page profile** lands in `users/firstname-lastname/` (created from `users/.template/`)

Both directories are gitignored — your data never gets committed by accident.

## Updates

**Update strategy: read-only `git pull`.** This repo ships content you use; you don't customize files inside it. To get the latest version:

```bash
git pull origin main
```

Your local data — `users/firstname-lastname/`, `session-records/`, plus runtime-internal `runtime/session-one/sessions/`, `runtime/session-one/feedback/`, `runtime/session-one/users/`, `runtime/session-one/outputs/` — is gitignored. It stays on your machine and is never touched by updates.

If you want to customize the script for your own use, fork the repo. If you have changes you'd like to contribute back, open a PR — `.gitignore` will prevent your personal session data from being staged.

## Privacy

When you use this tool, your inputs and outputs stay on your machine. This repo contains no telemetry. The published content is sanitized — no real user data, prompts, or examples reflect any individual. The included sample session (Carlos) is a fictional persona built for testing.

## Repo Structure

```
claude-self-portrait-sessions/
├── README.md                              (this file)
├── LICENSE                                (MIT)
├── CHANGELOG.md
├── .gitignore
├── runtime/
│   └── session-one/
│       ├── CLAUDE.md                      (Session Runner instructions — read by Claude)
│       ├── session-1-script.md            (the verbatim script — 14 screens)
│       ├── output-template.md             (the one-page profile artifact)
│       ├── generation-rules.md            (rules for the 4 live-generated fields)
│       ├── artifact-cleanup-guide.md      (how to clean a transcript into a shareable artifact)
│       ├── artifacts/_template.html       (HTML template for the shareable artifact)
│       └── examples/
│           └── sample-session-carlos.md   (a complete walkthrough)
├── users/
│   ├── README.md                          (explains where your multi-page profile lands)
│   └── .template/                         (the multi-page profile schema)
└── session-records/
    └── README.md                          (explains where each session's records land)
```

> v0.2.0 introduced the `runtime/` wrapper and promoted Session 1 to V2 (multi-page profile output). See [CHANGELOG.md](CHANGELOG.md) for the migration note.

## Support

This is a personal project shared as-is. File a [GitHub issue](https://github.com/19jzwiener/claude-self-portrait-sessions/issues) for bugs or unclear instructions. No SLA on responses, but I read them.

## Built by

[Joseph Zwiener](https://github.com/19jzwiener) — building self-understanding tools, learning to ship in public.

This is V2 of Session 1 of a longer journey. Session 2 — sharpening Your Name and your first move after a week of trying it — is coming. If you'd like to be notified, watch this repo.

## License

[MIT](LICENSE) — use it, fork it, build on it. Just don't claim you wrote it.

## Credits

The methodology draws on:
- **WOOP** (Wish, Outcome, Obstacle, Plan) — Gabriele Oettingen's mental contrasting + implementation intentions
- **Mom Test** discipline (Rob Fitzpatrick) — the post-session feedback protocol
- **Barnum calibration** — the rule that an archetype must couldn't-apply-to-80%-of-people to feel real
- The "negative surprise" + delayed Your Name reveal — designed by trial across multiple test sessions
