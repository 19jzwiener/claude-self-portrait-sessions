# Changes — Per-Page Evolution History

> Each file in `profiles/` here mirrors a file in `../profiles/` and tracks how that profile page has evolved across sessions.
>
> **Why this lives in a separate directory:** keeps profile pages tight (current state only, low token cost to read every session) while preserving full history when needed.
>
> **Structure:**
> - `artifact.md` — change log for the user's evolving artifact
> - `profiles/` — one change log per active profile page (mirrors `../profiles/`)
> - `inactive-profiles/` — change logs for retired profile pages (mirrors `../inactive-profiles/`)
>
> Read pattern: NEVER read these during default session prep. Only read when explicitly asked to surface evolution (e.g., "how has my pattern changed?") or during reviews.
