# Profile Templates

> **Created:** 2026-04-29
> **Purpose:** Templates for the multi-page user profile structure. Used for both real users (`life-prod-testing/users/[name]/`) and persona test runs (`life-prod-testing/personas/[name]/`).

---

## How to use

1. **Copy this entire directory** into the destination user/persona folder:
   - Real user: `cp -r users/.template/* users/[firstname-lastname]/`
   - Persona: `cp -r users/.template/* personas/[firstname-lastname]/`
2. **Rename `sessions/s01-YYYY-MM-DD.md`** to use the actual session date (e.g., `s01-2026-05-02.md`)
3. **Populate each page** by filling in `[bracketed placeholders]` from the just-completed session content
4. **Delete this README.md** from the copied destination — it's a template-only file, not a profile page

---

## Pages in the template

| File | Purpose |
|------|---------|
| `quick-profile.md` | Cheat sheet — read first |
| `identity.md` | Your Name + etymology + threads |
| `pattern.md` | Current pattern + active commitment |
| `language.md` | Symbolic vocabulary |
| `life-context.md` | People / places / projects / body / time |
| `runner-manual.md` | Operational notes for running their sessions |
| `system-issues.md` | V[N] issues traced to them |
| `sessions/s01-YYYY-MM-DD.md` | Frozen first-session record |

---

## Cross-reference

This template differs from `session-one-V2/users/_template.md`:

| Template | Purpose |
|----------|---------|
| `session-one-V2/users/_template.md` | V2-bound user *card* (operational scratch, single-file, V2-version-specific) |
| `users/.template/` (this) | Cross-version user *profile* (multi-page, persistent, refinable across sessions and script versions) |

For persona test runs in life-prod-testing, **only this template is required**. The V2 user card is optional (kept for parity with the V2 logging flow but redundant with the multi-page profile — testing will reveal whether to drop it).

---

## Architecture context

See `users/UPDATE-PROTOCOL.md` for the full post-session update protocol (Tier 1 / Tier 2, second-agent audit, stale-page diagnostic). For persona test runs, **most of UPDATE-PROTOCOL.md does NOT apply yet** — Session 1 is the only session that exists publicly, so there's no accumulated content to audit, no Tier 2 queue to surface, no stale pages to diagnose. Just the initial capture.
