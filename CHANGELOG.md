# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

> Pre-1.0 = API may change. Versions follow `0.MINOR.PATCH`.
> Per SemVer for 0.x: breaking changes bump MINOR (`0.1.0 → 0.2.0`), backward-compatible fixes bump PATCH.

## [Unreleased]

## [0.2.0] - 2026-05-04

### Added

- **`runtime/session-one/`** — Session 1 V2 promoted to public. Refined script (V1 → V2 changes: Screen 0 permission-to-interrupt, Screen 4 split into 3 micro-steps, Screen 6 "last one" drop, Screen 9 vector framing, Screen 12 negative-surprise generation rules, Screen 13 Your Name no-rename rule + reasons-it-feels-off carry-forward, plus 6 more — see commit history for the full list). Same 6-question intake, refined microcopy, validated across 11 pressure-test runs (1 real user + 10 personas).
- **`users/[firstname-lastname]/` — single user-rooted layout.** Everything about a user lives under one directory:
  - `artifact.md` — the user's current one-page profile, single file, evolves across sessions
  - `profiles/` — active profile pages (`quick-profile.md`, `identity.md`, `pattern.md`, `language.md`, `life-context.md`, `runner-manual.md`, `system-issues.md`) — current state only
  - `inactive-profiles/` — parking lot for retired dimensions
  - `raw/sNN-YYYY-MM-DD/` — verbatim per-session transcripts + feedback
  - `minutes/sNN-YYYY-MM-DD.md` — per-session narrative synthesis
  - `changes/` — evolution history per profile page + artifact
- **Schema at `users/.template/`** mirrors the same structure with placeholder files. Copied into the new user dir on first session.

### Changed

- **BREAKING — Repo restructure.** Runtime files moved from repo root into `runtime/session-one/` (was `CLAUDE.md`, `session-1-script.md`, `generation-rules.md`, `output-template.md`, `examples/` at root in v0.1.0). Anyone using v0.1.0 paths must update — `cd runtime/session-one` is the new working dir. Top-level now contains repo metadata + `runtime/` + `users/`.
- **BREAKING — Output paths.** Session output now writes entirely under `../../users/firstname-lastname/` (relative to `runtime/session-one/`). v0.1.0 wrote to root-level `sessions/`, `feedback/`, `users/{name}.md` (single-file). v0.2.0 consolidates all per-user data under one user-rooted directory.
- **Profile pages no longer carry change-log sections.** Evolution history moved out into a parallel `changes/` directory — keeps profile pages tight (constant token cost per read) while preserving per-page history for retrospective queries.
- **Single evolving artifact instead of per-session snapshots.** The artifact at `users/[name]/artifact.md` updates in place each session rather than creating a new snapshot file per run. Evolution preserved as a textual log at `changes/artifact.md`. Aligns with the product philosophy: the artifact represents who the user is *today*; past versions don't pin anyone to who they used to be.
- **`.gitignore`** simplified — single rule (`users/[a-z]*/`) excludes all real-user data. Legacy v0.1.0 patterns removed.
- Sample session `runtime/session-one/examples/sample-session-carlos.md` retained from v0.1.0 — still accurate as a session walkthrough.

### Why

- **Single user-rooted layout.** "Where is Jane's data?" should have one answer: `users/jane-doe/`. Previous v0.2.0 drafts split per-user data across `session-records/[date-name]/` AND `users/[name]/` — two top-level dirs holding overlapping content. Consolidating under one user root simplifies privacy (one path to gitignore), backup (one path to copy), deletion (one path to remove), and mental model.
- **Profile pages as current-state only.** Appending change logs to profile pages bloats the file linearly with session count, multiplying token cost on every session prep read. Moving change logs to a parallel `changes/` directory keeps profile pages constant-cost while preserving full history for the rare retrospective read.
- **Single evolving artifact.** The product's promise is "current best representation of who you are today." Holding outdated artifact snapshots tethers users to past versions of themselves. The minutes + change logs preserve evolution narratively without storing N versions of the artifact.
- **Multi-session scaling.** Putting `runtime/session-one/` in front future-proofs for `runtime/session-two/` etc. as the arc grows.

### Fixed

- **`.gitignore` rule that silently dropped a template file.** v0.1.0's broad `sessions/` rule was matching `users/.template/sessions/s01-YYYY-MM-DD.md` and excluding it from the public release. Fresh cloners would have hit a missing-template error during post-session capture. The new architecture removes the `sessions/` directory entirely (renamed via the user-rooted restructure) and removes the legacy gitignore rule.
- Missed dogfooding-fairness sanitization in `runtime/session-one/generation-rules.md` qualifier-construction example. Replaced "The Undeclared Builder" with "The Providing Stranger" to match the Carlos-derived calibration examples elsewhere in the file.

## [0.1.0] - 2026-04-27

### Added

- Initial public release of V1 Session 1 — a 15-minute self-discovery session you run with Claude Code.
- Verbatim 14-screen session script (`session-1-script.md`) — Phase A intake (6 questions) → reflection → Phase B artifact generation → Phase C commitment → Phase D compound hook + archetype reveal.
- Session Runner instructions (`CLAUDE.md`) — defines role, hard constraints, post-session feedback protocol (Mom Test discipline), and "if things break" appendix.
- One-page profile artifact template (`output-template.md`) — 7 fields: archetype name, signature, leak, vector + WOOP, negative surprise, checkpoints, gap questions.
- Live-generation rules (`generation-rules.md`) — rules for the 4 dynamically generated fields (3 vector options, flow-sized first move, negative surprise, archetype name + 3 gap questions) with quality checks and calibration examples.
- Sample session walkthrough (`examples/sample-session-carlos.md`) — fictional Carlos Mendez persona (48-year-old construction foreman) showing a complete session with iteration notes.
- MIT license.
- Read-only `git pull` update strategy. Personal session outputs (`sessions/`, `feedback/`, `users/`, `outputs/`) gitignored from upstream so contributors don't accidentally PR their personal data.

[Unreleased]: https://github.com/19jzwiener/claude-self-portrait-sessions/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/19jzwiener/claude-self-portrait-sessions/releases/tag/v0.2.0
[0.1.0]: https://github.com/19jzwiener/claude-self-portrait-sessions/releases/tag/v0.1.0
