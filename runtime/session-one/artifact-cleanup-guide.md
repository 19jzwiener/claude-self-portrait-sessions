# Artifact Cleanup Guide

> How to turn a raw Session 1 artifact (from `output-template.md`) into a clean, shareable page a user can read on their own and understand without the runner present.
>
> **Why this exists:** The raw artifact is structured for internal consistency. The shareable version has different constraints — it has to stand alone, read plainly, and feel like a personal page instead of a form output.
>
> **Source:** Learnings from Anita's 2026-04-22 session. See `iteration-log.md` for the raw findings behind each rule.

---

## Outputs

For each user, produce:

1. **HTML version** — `artifacts/YYYY-MM-DD-firstname-lastname.html` — the primary shareable artifact. Self-contained (inline CSS, no external dependencies), works on any device, opens in any browser, print-friendly, mobile-responsive. **This is what you send to the user.**
2. **Markdown version** — `artifacts/YYYY-MM-DD-firstname-lastname.md` — source of truth for the content, used internally + for git-friendly review.
3. **Plain-text version** — `artifacts/YYYY-MM-DD-firstname-lastname.txt` — fallback for direct email pasting without HTML rendering.

**Naming convention:** `firstname-lastname` (lowercase, hyphen-separated). If two people share the same name, add a context disambiguator (e.g., `john-smith-college`). See `CLAUDE.md` "Naming convention" section for the full rule.

### Primary delivery path

- **User has email:** attach the `.html` file, or "Print → Save as PDF" and attach the PDF.
- **User prefers physical:** open the `.html` in a browser and print — the print stylesheet is tuned for clean paper output.
- **User is on mobile only:** email the `.html` file as an attachment. It opens inline in most mobile mail apps.

### The template

The reusable template lives at `artifacts/_template.html`. To create a new user's artifact:

1. Copy `_template.html` to `artifacts/YYYY-MM-DD-firstname-lastname.html`
2. Find-and-replace all `{{PLACEHOLDER}}` tokens with the user's data (the template comment block at the top of the file lists every placeholder)
3. Apply the conditional removal rules (empty surprise addition, one-shot cadence, skipped "surprised by" question — see the template comments)
4. Open in a browser to verify formatting before sending
5. Update the user's card in `users/firstname-lastname.md` with the session history row pointing to the new artifact

---

## The Rules

### 1. Strip internal jargon

Forbidden in the shareable version (these are internal vocabulary only):

- **"Artifact"** — users don't know what this means. Use "page" or just the document itself.
- **"Vector"** — use "path," "direction," or "next step."
- **"Profile"** — use "page" or the user's name.
- **"Signature" / "Leak"** — drop the labels. Present the sentences directly.
- **"Phase A / B / C / D"** — these are session structure, not user-facing.

### 2. Lead with the stickiest element

Check the user's post-session Q4 ("single sentence from your profile page you'd remember tomorrow?"). Whatever they named is what stuck. Usually Your Name. Sometimes the surprise. Sometimes a specific sentence.

Lead with that. Put it high on the page, visually distinct.

For Anita: "Half present" → Your Name leads.

### 3. Add a plain-language gloss for the Screen 4 character name

The character name (e.g., "Hamster in a Wheel") caused downstream confusion in live sessions — users silently re-render what it means on each reuse. In the shareable page, add a one-sentence gloss right under the name using the user's own plain-words description of the pattern from Screen 4.

Template:
> **Your Pattern — [Character Name]**
>
> *(That's the name you gave it — [user's plain-words description of the pattern, drawn from their Screen 4 answer].)*

For Anita:
> **Your Pattern — Hamster in a Wheel**
>
> *(That's the name you gave it — the part of you that keeps repeating the same thoughts, wanting to shut it all out, feeling like life is just the to-do list on repeat.)*

### 4. Name the cadence of the chosen next step explicitly

The chosen path (from Screen 9) has a shape — daily habit, weekly, or one-shot. The raw template doesn't communicate this. The shareable page must.

After the plan, add one line:

- **Daily habit:** *"This is a daily thing — one morning at a time."*
- **Weekly:** *"This is a weekly thing — one [X] per week."*
- **One-shot:** *"This is a one-time move — done once this week."*

And the checkpoint section labels adapt to the cadence (see Rule 6).

### 5. Keep the landed version of the surprise

If Screen 12 went through multiple drafts (common — Screen 12 generation defaults to too-complex), use only the final version that landed. Do not show the failed drafts.

If the user added a nuance or extension after the surprise landed (common signal of a good surprise), include their addition as a callout:

> *(You added: "[their verbatim response to the surprise]." That's a real [case/nuance/insight] — worth keeping.)*

### 6. Rename the checkpoint labels

"Stretch date" / "Fair date" are internal labels. Rename to plain:

- **Daily habit:** "One-week check: [date] — if most of those 7 [mornings/days/etc.] held, you'd be proud." and "Two-week check: [date] — if most of those 14 held, that's a solid target."
- **One-shot:** "Check-in date: [date] — by then, the one thing done."
- **Weekly:** "One-week check" / "Two-week check" — adapt phrasing to the habit frequency.

Keep the "If both slip, we make the step smaller — no one's going to be mad at you" microcopy. That line is critical. Do not drop or soften.

### 7. Frame gap questions as "next time" prompts, not tests

The raw template presents Screen 13 gap questions as a list. In sessions, this reads as "questions you should be thinking about" — too much weight, especially after the Phase D cognitive load.

Reframe with a clear opener:

> ## Questions for Next Time
>
> These aren't for you to answer now. They're what I'd want to ask you when we meet again.
>
> - [Gap 1]
> - [Gap 2]
> - [Gap 3]

This gives the user permission to not hold them in mind, while still signaling continuity into Session 2.

### 8. Warm but neutral voice

The shareable page is from the product, not from the person who ran the session. Avoid:

- "We" (implies Claude + user, reads awkwardly in text)
- "I" written as if the runner is speaking (confusing — was it Claude? Joseph? the product?)

Prefer:
- Direct second-person: "You can keep any part of it."
- Neutral product voice where necessary: "That's the name I'd put on what came through tonight" (singular "I" is OK when it reads as the product's voice, not a specific person).

### 9. Opener and closer

**Opener** — 2-3 lines at the top framing this as a growing, iterative page (not a verdict to accept-or-reject). Forward-looking, not defensive:

> This is the current view we created of you. It will continue to improve and change in future sessions. Step 1 is done — but there's much more to discover in the sessions ahead.

**Why this framing (not "you can reject it"):** The "keep it / change it / reject it" framing sounds defensive and reads as if the product expects pushback. The forward-looking frame positions the page as a living artifact that grows with each session — matches the 10-session arc philosophy (Breadth S1-3 → Lean S4-6 → Compound S7-10) baked into the product.

**Your Name sub-note** — under the Your Name callout, one short line signaling the name is a starting point, not a verdict:

> The name we're starting with. It'll keep evolving.

Do NOT use "keep it, change it, or say no to it" framing — same defensive tone problem as the old opener.

**Closer** — the V1 + Session 2 promise, kept honest, plus an explicit feedback invitation:

> *This is Version 1. We'll make it sharper together next time.*
>
> *Everything on this page is subject to change based on your feedback. If something feels off or doesn't fit, tell me — that's how the next version gets sharper.*

Two lines, not one. The first line is the V1 + next-session promise. The second line explicitly invites feedback — this matters because users (especially non-technical pilot users like Mom) don't assume they can critique something that looks polished. The invitation has to be stated, not implied.

Do not promise Session 2 if there is no intent to deliver it. Do not soften the "V1" framing — users should know this is iterative.

### 10. Plain-text version formatting

For the `.txt` email-paste version:

- ALL CAPS for section headers (not markdown `#`)
- Blank lines for separation (not `---` horizontal rules that render as dashes)
- Indent quoted content with 3 spaces (not `>` blockquote syntax)
- Use `--` for em-dashes (some email clients mangle `—`)
- Line length ≤ 72 characters for universal compatibility
- No backticks, no asterisks for emphasis — just structure through spacing and caps

---

## Checklist (run before sending) — V2 update

- [ ] No "artifact" / "archetype" / "vector" / "signature" / "leak" / phase-labels in user-facing copy *(V2 — "profile" / "profile page" is now an OK user-facing word; "signature" added to banned list since it's now the V1 label being replaced; "archetype" added as the original V1 term that should never appear user-facing)*
- [ ] Your Name handle present near top (label says "Your Name", content is the 3-5 word generated handle)
- [ ] Stickiest element from Q4 is near the top
- [ ] Character name (Screen 4) has a plain-language gloss below it (per Screen 4c reflect-back)
- [ ] Chosen path cadence is named ("daily thing" / "weekly" / "one-time")
- [ ] Checkpoint labels match cadence, not "Stretch/Fair"
- [ ] Surprise is the final landed version only — concrete user-examples + plain contrast (NOT abstract-mechanism per V2 generation rules)
- [ ] Gap questions framed as "next time" with explicit permission not to hold them now
- [ ] Opener uses forward-looking framing ("current view that will evolve") — NOT V1's defensive "keep/change/reject" framing
- [ ] Your Name has "does this sound right?" framing — NOT V1's "keep/say no/rename" buttons (V2 product decision 2026-04-28)
- [ ] Closer is V1 + next-time honest promise
- [ ] HTML version produced from `_template.html` with all `{{PLACEHOLDERS}}` replaced
- [ ] HTML opens correctly in a browser (verify before sending)
- [ ] Conditional sections handled (surprise addition, cadence-dependent checkins, surprised-by question)
- [ ] Markdown + plain-text versions also produced for internal / fallback use
- [ ] Plain-text version ≤ 72 char lines, no markdown syntax

---

## Session-by-session learning

This guide updates as more sessions happen. When a new session surfaces a cleanup pattern not covered here, add it. Use the iteration log for raw findings; use this guide for durable rules.

### Change log

| Date | Added | Based on |
|------|-------|----------|
| 2026-04-23 | Initial guide — 10 rules | Anita 2026-04-22 session (see `iteration-log.md`) |
| 2026-04-23 | Added HTML output as primary format + `_template.html` workflow for reusable per-user generation | Joseph request — need a formatted page she can open in browser, download, send |
| 2026-04-23 | Rewrote Rule 9 opener/archetype-subnote to forward-looking frame ("current view that will evolve") instead of defensive "keep/change/reject" frame | Joseph feedback — old framing sounded apologetic, new framing positions page as a living artifact matching the 10-session arc |
| 2026-04-23 | Added explicit feedback-invitation line to the closer on all page types (artifact, preview, arc). Two-line footer: V1 promise + feedback invite | Joseph request — pilot users don't assume they can critique a polished-looking page; the invitation has to be stated |
| 2026-04-23 | Updated all file-path examples to `firstname-lastname` naming convention. Added note about `users/firstname-lastname.md` card update after artifact generation | Schema rollout — first+last+email+source captured at intake; user cards track context + Your Manual across sessions |
