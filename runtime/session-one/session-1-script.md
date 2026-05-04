# Session 1 — Script

> **Time budget:** ~30-45 minutes
> **Outcome:** User walks away with a one-page profile (see `output-template.md`) plus a multi-page profile in `../../users/firstname-lastname/`
> **Runner:** Read each screen's user-facing content **verbatim**. Do not paraphrase.

---

## Time Budget

| Phase | Duration | Screens |
|-------|----------|---------|
| Welcome | 60s | Screen 0 |
| Phase A — Intake | ~25 min | Screens 1-6 |
| Reflection | 90s | Screen 6.5 |
| Phase B — Artifact | 5 min | Screens 7-9 |
| Phase C — Commitment | 4 min | Screens 10-11 |
| Phase D — Compound Hook | 3 min | Screens 12-13 |
| **Total** | **~40 min** | 14 screens |

**Note for runner:** Tell the user up front this takes 30-45 min. Honest framing protects trust when they hit Screen 4 or Screen 12 and need real time to think. Screens 2 and 4 are the big-think screens — let them breathe.

---

## SCREEN 0 — Intake + Welcome (60s)

**[Runner: Before reading the welcome, capture intake metadata. These are NOT user-facing script lines — they're quick admin asks to set up the session file correctly. Keep it conversational, not form-like.]**

**Intake fields to capture:**
1. First name
2. Last name
3. Email address (so the artifact can be sent and Session 2 can be scheduled)
4. Source / context (runner's note — how did they hear about this? — may already be known from the intake email)
5. Today's date (confirm)

**Runner action:** Check if `../../users/firstname-lastname/` already exists (the multi-page profile dir).
- **If it exists** — this person has done a session before. This is Session 2+. The current Session 1 release does not cover that flow — tell the user this is for first-time sessions and ask them to confirm they want to start fresh.
- **If it doesn't exist** — proceed to the welcome script below. The multi-page profile will be created during the post-session capture step (see `CLAUDE.md` for steps).
- **If a directory with the same `firstname-lastname/` exists for a DIFFERENT person** — add a disambiguator (e.g., `john-smith-college/`). Confirm the disambiguator with the user before proceeding.

---

**[You say/write to the user — verbatim]:**

> Hey. Before we start — this isn't a personality quiz.
>
> The whole thing takes about 30 to 45 minutes. You'll answer 6 questions, then we'll work together to turn your answers into a one-page profile — sentences in your own words, a name for the pattern that throws you off, and one concrete next step. Some questions might feel weird. The 3 sentences you write about yourself are the point.
>
> I'm not going to label you. I'm going to ask the right questions in the right order. So you can finally say out loud something you already half-know about yourself.
>
> **Feel free to ask questions or ask for more context at any point. If something doesn't land, tell me — we'll work through it together.**
>
> Ready?

**[User responds with "yes" / "ready" / equivalent.]**

[RUNNER NOTE: If they ask questions, answer briefly and redirect to starting. If they seem hesitant, ask: "Is something unclear?" but do not re-explain the session. The permission-to-interrupt line opens the channel for users who need real-time clarification on screens 4, 10, and 12 but don't know they can ask.]

---

# PHASE A — Intake (~25 min)

## SCREEN 1 — Domain-Naming (60s)

**[You say/write — verbatim]:**

> Pick the 4-6 parts of your life that matter most to you right now. Don't think too hard — go with your gut.
>
> Choose from these (or write your own):
>
> - Work / Job
> - Money
> - Dating / Romance
> - Friendships
> - Family
> - Health / Body
> - Play
> - Making things
> - Learning
> - Purpose
> - Something else: _______
>
> Just list the ones you pick.

**[User lists 4-6 domains.]**

[RUNNER NOTE: Capture their list verbatim. Accept any they write in. Do not comment on choices.]

---

## SCREEN 2 — Peak-Moment Scene (3-5 min)

**[You say/write — verbatim]:**

> Take 30 seconds before you start typing — land on **one** moment, then write.
>
> Write about ONE moment in the last month when you felt **most alive** or **most like yourself.** Just one — a single scene, not a list.
>
> Full sentences, starting with "I." Don't polish it — nobody reads this but you and me. Just tell me about that one scene: where were you, what were you doing, what did you feel. 3 to 5 sentences about that one moment.

**[User writes ONE peak-moment scene in 3-5 sentences.]**

[RUNNER NOTE: If they list multiple scenes, accept what they wrote (still usable data) but capture the multi-scene response in their transcript. The 30-sec think cue + explicit "ONE moment, not a list" framing exists because users sometimes interpret "3-5 sentences" as scene-count rather than depth on one scene. If they give a one-line answer, prompt once: "Can you give me a few more details about that ONE scene? Where were you, what were you doing, what did it feel like?" If they refuse or can't, accept what they wrote and move on.]

---

## SCREEN 3 — Envy Prompt (2 min)

**[You say/write — verbatim]:**

> Who do you envy — and what *exactly* about them?
>
> If a few people come to mind, write them all first. It's fine to be broad here.
>
> Then, underneath: **which one feels sharpest? That's the one we'll use.** Be honest. Envy is a clue. I'm just trying to read it.

**[User lists a few people, then narrows to one. Capture both the broad list and the one chosen.]**

[RUNNER NOTE: This is split into 2 steps within one screen so users get permission-to-be-broad-first before committing. Pilot users hesitated on a "one person" constraint not because of envy but because of commit-before-warmup. The broad list is throwaway; the narrowed-to-one is the data Screen 9 generation uses. If they say "I don't envy anyone," try once: "Not even a small thing? Someone whose life or approach makes you notice it — even in a small way?" If they still say no, move on.]

---

## SCREEN 4 — Externalize the Pattern (5-8 min — split into 4a / 4b / 4c)

**[NOTE for runner:** This is the most important — and most cognitively demanding — screen. The 3 micro-step structure exists because the leap from "describe the pattern" to "give it a character" is too big to do in one move. The user describes the pattern in their own plain words FIRST, then names it as a character, then the runner reflects the name back tied to the user's plain words to lock shared meaning before any downstream screen reuses the character name. Do NOT offer example character names upfront — that anchors users on the runner's metaphors instead of their own language.**]**

---

### Screen 4a — Describe the pattern in plain words (2-3 min)

**[You say/write — verbatim]:**

> There's a pattern that keeps throwing you off. Before we name it, just describe what it actually does — in plain words, your own language.
>
> What does this pattern look like when it's running? What does it make you do, or stop you from doing? When does it usually show up?

**[User describes the pattern in plain language. This is the foundation — capture verbatim.]**

[RUNNER NOTE: Do NOT offer character framings yet. Just the plain description. If they jump straight to a character name, gently redirect: "Hold that — first describe what it actually does, then we'll give it a name in a minute."]

---

### Screen 4b — Name it as a character (2-3 min)

**[You say/write — verbatim, after they finish 4a]:**

> Now: pretend that pattern is a character. Someone separate from you, with a name and a feel. What would you call it?
>
> It can be anything — a villain, an animal, an object, an imagined person, a single word — just a name that fits how it feels to you.

**[User offers a character name. Capture verbatim.]**

[RUNNER NOTE: If they struggle, offer support — but DO NOT offer specific names. Try: "What comes to mind first? Don't filter — what's the first thing that pops up when you imagine that pattern as a character?" If still stuck after 2 prompts, accept "the pattern" or whatever neutral term they prefer. Do not push.]

---

### Screen 4c — Reflect-back confirmation (lock shared meaning before reuse)

**[You say/write — verbatim, substituting [character name] with what they offered in 4b and [user's plain-words pattern] with the language from 4a]:**

> So when I say **[character name]**, I mean **[user's plain-words pattern from 4a — paraphrase tightly using their own words]**.
>
> That's what we'll use in the next few questions. Does that match what you meant?

**[User confirms or corrects. If they correct, accept the correction and re-confirm before proceeding.]**

[RUNNER NOTE: This step is non-negotiable. Real-pilot data showed downstream re-rendering load — every time the character was reused (Screens 8, 12, 13), users silently re-decoded what it meant. The 4c reflect-back locks shared meaning ONCE so reuse is frictionless. If they correct your paraphrase, capture the correction in their transcript file — your model of their pattern was wrong.]

---

### After 4c — capture both halves of the pattern

**[You say/write — verbatim]:**

> Two more things about **[character name]**:
>
> What does it **do to you** when it's running? (You may have covered this already in 4a — feel free to repeat or add to it.)
>
> And when does it have **less hold** on you?

**[User answers both halves. Capture verbatim.]**

[RUNNER NOTE: The "less hold" half is critical for Screen 8 (leak frame) and Screen 9 (vector generation). If they only answer one half, prompt: "And the other one — when does it have less hold on you?" Capture both halves before moving to Screen 5.]

---

## SCREEN 5 — Situational Scenario (60s)

**[You say/write — verbatim]:**

> Quick question. Just type your gut reaction.
>
> **It's Sunday night. You meant to do 3 things this weekend. None of them are done. What do you actually do?**

**[User answers — gut response.]**

[RUNNER NOTE: Do not accept abstraction. If they answer "I'd be stressed," prompt: "What would you actually DO though? What's the behavior?"]

---

## SCREEN 6 — Chapter Title (60s, gut response)

**[You say/write — verbatim]:**

> Last question in this first part.
>
> Pretend someone is writing your life story. The chapter you're in **right now** — what would they call it?
>
> One line. First thing that pops into your head. Don't overthink it — your gut answer is the right one.

**[User gives a chapter title.]**

[RUNNER NOTE: Use "Last question in this first part" — it's honest because more is coming after Phase A. Saying "Last one." (without qualification) creates a relief response, then breaks trust when 7 more screens follow. Accept their first answer. If they start over-thinking or editing, say: "Your first instinct is the right one. Go with what came first."]

---

## Phase A → Phase B Bridge (30s, breath)

**[You say/write — verbatim, after Screen 6 is captured]:**

> That's the intake done. The rest of the session uses what you just wrote — it gets lighter from here.

**[Brief pause — let them breathe before moving to Reflection (Screen 6.5).]**

[RUNNER NOTE: Phase A is the heaviest cognitive lift in the session — by the end of it, users are tired and often visibly so. The bridge line resets expectations for Phase B+ and acknowledges the lift. One sentence. Don't elaborate.]

---

# INTERLUDE — Reflection Screen (90s)

## SCREEN 6.5 — "Here's What You Wrote"

**[You say/write — verbatim]:**

> Before we build anything — here's what you wrote. Same words, no changes. Read it to yourself.
>
> **Your big moment:**
> *[Paste verbatim from Screen 2]*
>
> **Who you envy, and what about them:**
> *[Paste verbatim from Screen 3]*
>
> **Your pattern (and when it loses its hold):**
> *[Paste verbatim from Screen 4]*
>
> **What you do on Sunday nights:**
> *[Paste verbatim from Screen 5]*
>
> **The chapter of your life you're in right now:**
> *[Paste verbatim from Screen 6]*
>
> Take 30 seconds. Does this look like you?
>
> Options:
> - "Yeah, that's me. Let's keep going."
> - "Something's off — let me fix one."

**[User confirms or edits.]**

[RUNNER NOTE: If they want to edit, accept the edit and update the captured answer. Do not push back. Do not ask "why" unless they volunteer.]

---

# PHASE B — Artifact Generation (5 min) — FRAMES, NOT DRAFTS

## SCREEN 7 — Your Signature (90s)

**[You say/write — verbatim]:**

> Using your own words from the last 6 minutes, finish these two sentences. Don't overthink it. Pull straight from what you just wrote.
>
> **"I come alive when ____."**
>
> **"I drift when ____."**

**[User writes both sentences. Do NOT offer a draft. Do NOT give examples. They fill from zero.]**

[RUNNER NOTE: If they ask for help, say: "Pull from the peak moment you wrote in Screen 2, and the pattern you named in Screen 4. Use your own phrasing." Do not draft for them.]

---

## SCREEN 8 — Your Leak (60s)

**[You say/write — verbatim, substituting [Character] with whatever the user named on Screen 4]:**

> You named a character earlier. Write one sentence about what they do to you. And one sentence about when they lose power.
>
> **"[Character name] does this to me: ____."**
>
> **"[Character name] loses power when ____."**

**[User writes both sentences.]**

[RUNNER NOTE: If they didn't name a character on Screen 4 (rare), use the neutral frame: "The pattern that hijacks me does this to me: ___" and "The pattern loses power when ___." Substitute the specific language they did use.]

---

## SCREEN 9 — Three Directions (3 min)

**[You generate 3 directions using `generation-rules.md` and the user's data from Phase A. Each direction is tagged with its cadence: daily habit / once this week / weekly. Then say/write — verbatim]:**

> Based on what you wrote, here are three directions you could take over the next 1 to 2 weeks to work on one of the struggles I've identified. Pick the one that feels like a stretch — something you're not already doing. We'll make it real in the next step.
>
> **Option 1 — [Plain-action title, no metaphor] ([cadence — daily habit / once this week / weekly]):** [1-2 sentence specific direction with a concrete first move]
>
> **Option 2 — [Plain-action title, no metaphor] ([cadence]):** [1-2 sentence specific direction]
>
> **Option 3 — [Plain-action title, no metaphor] ([cadence]):** [1-2 sentence specific direction]
>
> Pick one, edit one, or say no to all three.

**[User picks one, edits one, rejects all, or writes their own.]**

[RUNNER NOTES — design rules for this screen:
1. **"Vector" dropped from user-facing copy.** Replaced with "directions / paths / options." Pilot users were confused by the word. Keep "vector" internally in generation-rules.md and session files; never user-facing.
2. **Frame line added at top:** *"Based on what you wrote, here are three directions you could take over the next 1 to 2 weeks…"* — names Claude as the source of the options, ties to Screen 11 Stretch/Fair (7/14 days), tells the user what the screen IS FOR.
3. **Option titles must be plain-action descriptions, NOT metaphors.** Bad: "Eat One Meal On Your Own Side." Good: "Eat one meal without judging yourself." Keep concept, drop metaphor.
4. **Generation rule — DO NOT offer options the user is already doing.** Filter generated options against Screen 2 + 4 + 5 data. If an option overlaps with existing behavior, regenerate it. Options must stretch, not confirm.
5. **Cadence tag REQUIRED on each option.** "(daily habit — 20 min each morning)" or "(once this week — one meal)" or "(weekly — one practice session)". User sees the commitment shape before picking. Cadence cascades to Screen 10 (only fires for daily habits) and Screen 11 (framing adapts).
6. **Generation rule — prefer daily-habit options when user data supports both.** Habits compound; one-shots don't. Envy data skews toward one-shots by construction; treat envy as a *direction signal* (what does the user wish they had?), then translate into a repeatable practice.
7. **If they say "Option X is right but I'm avoiding it"** — capture verbatim, that's gold for Session 2. Do not comment in the moment.]

---

# PHASE C — Commitment (4 min)

## SCREEN 10 — Habit Stacking (4 min — split into 10a / 10b / 10c)

**[NOTE for runner:** This screen splits three asks (accept first move + pick trigger from menu + assemble IF/THEN) into separate sub-steps and reframes around **habit stacking** (Atomic Habits / BJ Fogg shorthand most users have prior exposure to) instead of explaining WOOP from scratch. Combining all three into one prompt is too dense to land without live runner interpretation. **This screen ONLY fires for daily-habit cadence options** (per Screen 9 cadence tag). For once-this-week or weekly options, skip 10b habit-stacking entirely and go straight to 10c IF/THEN with a date-based trigger.**]**

---

### Screen 10a — First move, accept or edit (90s)

**[You say/write — verbatim, substituting [chosen direction] with what the user picked on Screen 9]:**

> You picked **[chosen direction]**. Let's make it real.
>
> Your first move (15-30 minutes, a small stretch from where you are) is:
>
> **[Generated from their direction + leak data — specific, doable, shippable this week]**
>
> Does that feel doable? You can edit it, or say no and we'll build a different one.

**[User accepts, edits, or rejects. If they reject, ask one clarifying question and regenerate.]**

---

### Screen 10b — Habit stacking framing (90s) — ONLY for daily-habit cadence

**[You say/write — verbatim, after they accept the first move and IF the option is a daily habit]:**

> This is **habit stacking** — we pair your new move with something you already do every day, so the existing thing becomes the reminder. That way the trigger does the work for you.
>
> Two questions to find the right pair:
>
> **(1) When during the day would be the ideal time for you to do this?**
>
> **(2) What do you already do around that time that we could stack onto?**

**[User answers both. The trigger comes from their life, not a fixed menu — automatically filters out triggers that don't match the new habit's timing.]**

[RUNNER NOTE: An earlier fixed trigger menu (Sunday coffee / Friday laptop close / etc.) was replaced with these two narrowing questions. The fixed menu often didn't fit; users either had to force a fit or write in. The narrowing questions surface a personal trigger every time. **For one-shot or weekly options:** skip 10b entirely. The trigger is a date, not a habit-stack. Go straight to 10c with: "When this week will you do it?"]

---

### Screen 10c — Assemble IF/THEN (60s)

**[You say/write — verbatim, having taken the daily-habit answers from 10b OR the date-based answer for one-shot/weekly]:**

> Then we write it like this:
>
> **IF** [the trigger from 10b — or, for one-shot, the chosen date]
> **THEN** [the action from 10a]
>
> Read it out loud once. Does it feel doable?

**[User confirms or edits. Write their final IF/THEN statement verbatim in the session file.]**

[RUNNER NOTE: Reading it out loud is the felt-sense check. If they hesitate, ask: "What's making it not feel doable? Too big? Wrong time? Wrong trigger?" Adjust whichever element they name.]

---

## SCREEN 11 — Checkpoints (90s — framing adapts to cadence)

**[NOTE for runner:** Checkpoint framing must match the cadence tagged on the chosen Screen 9 option. An earlier "Stretch / Fair" framing only made sense for daily habits — for one-shot moves (e.g., "1 meal eaten") it was nonsensical ("most of 7 times you ate one meal"?). Use the right framing below based on cadence.**]**

---

### IF the chosen direction is a DAILY HABIT:

**[You say/write — verbatim]:**

> Three dates to check in on yourself:
>
> **Stretch date** (you'd be proud if you hit this — *most of 7 mornings the new habit held*): **[suggest today + 7 days]** — you can change it
>
> **Fair date** (a reasonable target — *2 weeks in, the trigger is sticky*): **[suggest today + 14 days]** — you can change it
>
> **If you miss both:** we sit back down and figure out what's in the way. No one's going to be mad at you. We'll just make the step smaller.

---

### IF the chosen direction is a ONE-SHOT (once this week):

**[You say/write — verbatim]:**

> One date to mark:
>
> **By [suggest today + 7 days]:** the one thing done. — you can change the date
>
> **If it doesn't happen:** we sit back down and figure out what got in the way. No one's going to be mad at you. We'll just make the step smaller.

---

### IF the chosen direction is WEEKLY (one practice per week):

**[You say/write — verbatim]:**

> Two checkpoints:
>
> **By [suggest today + 7 days]:** first session done. — you can change the date
>
> **By [suggest today + 14 days]:** 2 weeks in a row. — you can change the date
>
> **If you miss both:** we sit back down and figure out what's in the way. No one's going to be mad at you. We'll just make the step smaller.

---

**[User confirms or edits dates.]**

[RUNNER NOTE: Use concrete calendar dates, not "in a week." Calculate from today's date. The "won't be scolded" microcopy is critical — read it verbatim regardless of cadence.]

---

# PHASE D — Compound Hook + Your Name Reveal (3 min)

## SCREEN 12 — Your Negative Surprise

**[You generate the negative surprise using `generation-rules.md` and the user's signature + leak data. Then say/write — verbatim]:**

> One thing before we finish. You might not want to hear this — but it's worth sitting with.
>
> **[Generated negative surprise — 1-2 sentences using user's own vocabulary, following the strength-becomes-leak template]**
>
> How does this land for you?

**[User reacts in 1-2 sentences. Capture verbatim.]**

[RUNNER NOTE: Do not soften the surprise. Do not apologize. Do not walk it back if they flinch — the flinch is the feature. If they reject it ("that's not me"), capture that too and move on. Do not defend.]

---

## SCREEN 13 — Your Name Reveal + Gaps + Honest Hook (split into 13a / 13b)

**[NOTE for runner:** Two design rules for this screen. **(1)** Split into 2 beats so Your Name lands and registers BEFORE the 3 gap questions arrive. Real pilots showed Your Name landing strongly while the gap questions evaporated when delivered together — the screen was too dense to let both register. **(2)** Users do NOT rename Your Name in this session. Instead the runner asks "Does this sound right?" — if yes, keep moving. If not, the user writes reasons it feels off, and the runner promises Session 2 will discuss those reasons and figure out why it doesn't quite hit. The reasons-it-feels-off become Session 2 input, not a renaming exercise inside Session 1.**]**

---

### Screen 13a — Your Name Reveal + "Does this sound right?" (90s)

**[You generate the Your Name handle using `generation-rules.md`. Then say/write — verbatim, substituting [Your Name] with what you generated]:**

> A name for all of this: **[Your Name — 3-5 words, Barnum-calibrated, specific to their signature + leak]**.
>
> **[1-sentence description of what this name means in their context, using their own language from earlier screens]**.
>
> Does this sound right?

**[User responds.]**

**IF the user says yes / "yeah, that's me" / "feels right" / equivalent:**

**[You say/write — verbatim]:**

> Good. We'll keep this as a working handle. It's not a verdict — it's a starting point. We'll come back to it in Session 2 and see how it holds up.

→ Move to Screen 13b.

**IF the user says no / "feels off" / "not quite right" / equivalent:**

**[You say/write — verbatim]:**

> Got it. Tell me what feels off about it — in your own words. Doesn't have to be polished. What does the name miss, or get wrong, or land too heavy on?

**[User writes reasons-it-feels-off in their own words. Capture verbatim under a `reasons_name_feels_off` field in the session file.]**

**[Then you say/write — verbatim, after they're done:]**

> Thanks. I'm not going to retitle it tonight — the reasons you just wrote are exactly what we'll dig into in Session 2 together. We'll figure out why this name doesn't quite hit and find one that does. For now, it's a placeholder.

→ Move to Screen 13b.

[RUNNER NOTE: Users do NOT rename Your Name inside Session 1. Reasons-it-feels-off becomes Session 2 input. **Do NOT** offer to retitle on the spot. **Do NOT** suggest alternative names. The user's resistance is data for Session 2, not a problem to solve in Session 1. Capture the reasons verbatim — those are the highest-signal Session 2 inputs you'll get.]

---

### Screen 13b — Gap Questions + S2 Framing (90s)

**[You generate 3 gap questions using `generation-rules.md`. Then say/write — verbatim]:**

> Here are three things I don't know about you yet — these are the threads we'll pull on next time:
>
> - **[Generated gap question 1 — open, specific to their session data]**
> - **[Generated gap question 2 — open, specific to their session data]**
> - **[Generated gap question 3 — open, specific to their session data]**
>
> You don't need to answer these now. They're for you to notice between now and Session 2.
>
> ---
>
> **This is Version 1 of your profile. Next time, we'll make it sharper together. I'll show you this again, ask what still fits, and fill in the gaps you just saw.**
>
> One line before you go (you can skip this): **what surprised you today?**

**[User optionally answers the surprise question. Capture verbatim if they answer.]**

[RUNNER NOTE: Gap questions are framed as "things to notice between now and Session 2," not as questions the user must hold in mind right now. Lighter cognitive load + extends the session beyond the 40 min. The "this is the first version, we'll sharpen it next session" line is NOT a marketing hook — it's an honest promise that must be mechanically fulfilled in a real Session 2 one week later. Do not say this if Session 2 isn't actually going to happen.]

---

# END OF SESSION

After Screen 13:

1. Generate the final artifact at `../../users/[firstname-lastname]/artifact.md` using `output-template.md` rules + `artifact-cleanup-guide.md` rules
2. Write the verbatim transcript to `../../users/[firstname-lastname]/raw/s01-YYYY-MM-DD/transcript.md`
3. Begin the post-session feedback protocol (see `CLAUDE.md` for the 5 Mom Test questions)
4. Capture feedback in `../../users/[firstname-lastname]/raw/s01-YYYY-MM-DD/feedback.md`
5. Capture any friction or unusual moments alongside the user's other answers in the transcript or feedback file
6. Run the post-session profile capture step (see `CLAUDE.md` "Post-session profile capture" section) — populates the multi-page profile, the per-session synthesis at `minutes/`, and initial entries in every change log

---

## Appendix — What To Do If Things Go Sideways

| Situation | What you do |
|-----------|-------------|
| User answers one-liner on Screen 2 (peak moment) | Prompt once for more detail. If they can't or won't, accept what they wrote. |
| User says "I don't envy anyone" on Screen 3 | Prompt once for even a small thing. If still no, move on. |
| User can't name a character on Screen 4 | Offer: "It can be anything — villain, animal, object, just a name. What comes to mind?" If still blank, use generic "the pattern" wording downstream. |
| User skips more than 2 Phase A screens | Pause the session. Explain: "We need at least 4 of 6 answers to build something meaningful. Continue or stop?" |
| User cries / gets emotional | "Take whatever time you need. We can pause or stop entirely — your call." Do not rush them. |
| User says "this is bullshit" mid-session | Capture verbatim in their feedback file. Ask: "What specifically isn't landing? We can stop or adjust." |
| User's answers seem performative / fake | Do not call it out in the moment. Note in their feedback file after the session. |
| User wants to see what you're writing / generating | Show them. Transparency is fine. |
| User asks "what's the right answer?" | "There isn't one. Just your actual answer." |
