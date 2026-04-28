# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Fixed

- Missed dogfooding-fairness sanitization in `generation-rules.md` qualifier-construction example (line 158). Replaced "The Undeclared Builder" with "The Providing Stranger" to match the Carlos-derived calibration examples elsewhere in the file. Caught when re-scanning after a cross-machine merge surfaced the leak.

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
