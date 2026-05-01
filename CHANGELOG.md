# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

> Pre-1.0 = API may change. Versions follow `0.MINOR.PATCH`.
> Per SemVer for 0.x: breaking changes bump MINOR (`0.1.0 → 0.2.0`), backward-compatible fixes bump PATCH.

## [Unreleased]

## [0.2.0] - 2026-05-01

### Added

- **`runtime/session-one/`** — Session 1 V2 promoted to public. Refined script (V1 → V2 changes: Screen 0 permission-to-interrupt, Screen 4 split into 3 micro-steps, Screen 6 "last one" drop, Screen 9 vector framing, Screen 12 negative-surprise generation rules, Screen 13 Your Name no-rename rule + reasons-it-feels-off carry-forward, plus 6 more — see commit history for the full list). Same 6-question intake, refined microcopy, validated across 11 pressure-test runs (1 real user + 10 personas).
- **`users/`** — multi-page profile schema. After Session 1 ends, the Session Runner creates `users/firstname-lastname/` with 7 structured pages (`quick-profile`, `identity`, `pattern`, `language`, `life-context`, `runner-manual`, `system-issues`) plus `sessions/s01-YYYY-MM-DD.md` for the frozen per-session record. The schema lives at `users/.template/`. This is V2's main output upgrade — V1 produced only a single-page artifact; V2 produces the artifact AND a compounding multi-page profile that future sessions can build on.
- **`session-records/`** — per-run directories. Each session's transcript, feedback, and shareable artifact (HTML/MD/TXT) land in `session-records/YYYY-MM-DD-firstname-lastname/`. Replaces the old V1 layout where these scattered into separate `sessions/`, `feedback/`, and `artifacts/` dirs.
- **Skeleton READMEs** in `users/` and `session-records/` documenting where data lands.

### Changed

- **BREAKING — Repo restructure.** Runtime files moved from repo root into `runtime/session-one/` (was `CLAUDE.md`, `session-1-script.md`, `generation-rules.md`, `output-template.md`, `examples/` at root in v0.1.0). Anyone using v0.1.0 paths must update — `cd runtime/session-one` is the new working dir. Top-level now contains repo metadata only: `README.md`, `LICENSE`, `CHANGELOG.md`, `.gitignore`, `runtime/`, `users/`, `session-records/`.
- **Output paths.** Session output now writes to `../../session-records/YYYY-MM-DD-firstname-lastname/` (transcript + feedback + artifact) and `../../users/firstname-lastname/` (multi-page profile), both relative to `runtime/session-one/`. v0.1.0 wrote to root-level `sessions/`, `feedback/`, `users/{name}.md` (single-file).
- **`.gitignore`** patterns updated for the new layout — both root-level (`users/firstname-lastname/`, `session-records/`) and runtime-internal (`runtime/session-*/sessions/`, etc.) personal data dirs.
- Sample session `examples/sample-session-carlos.md` retained from v0.1.0 — still illustrative of the session flow. Note: it shows V1's single-page artifact format; V2 produces the multi-page profile in `users/`. See `users/.template/` for the V2 schema.

### Why

- **Multi-session scaling.** v0.1.0's flat root structure assumed one session. Putting `runtime/session-one/` in front future-proofs for `runtime/session-two/` etc. as the arc grows.
- **Data architecture upgrade.** V2's multi-page profile is a more honest representation of who someone is than a single page. Each page captures a different dimension; together they compound across sessions instead of being overwritten.
- **Mirror parity with private dev environment.** The same `runtime/session-one/` structure exists in Joseph's private dev repo — public users get exactly what gets dogfooded.

### Fixed

- Missed dogfooding-fairness sanitization in `runtime/session-one/generation-rules.md` qualifier-construction example (line 158). Replaced "The Undeclared Builder" with "The Providing Stranger" to match the Carlos-derived calibration examples elsewhere in the file. Caught when re-scanning after a cross-machine merge surfaced the leak.

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
