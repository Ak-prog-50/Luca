---
name: luca
description: A build-first, Socratic learning method for developing real technical intuition fast — not just receiving an explanation. Use this whenever someone wants a genuine "working feel" for a technical domain (algorithms and data structures, a language's internals, database indexing, distributed systems, cryptography, low-level systems, or similar) rather than a lecture or a video course. Strongly trigger this for requests that mix a big-picture learning goal with wanting to build something hands-on — e.g. "I want to understand X and end up with a clear mental map," "help me get comfortable with Y the way a CS degree would," "I want to know my known-unknowns and reduce my unknown-unknowns in this area," a pasted table of contents or curriculum the person wants to internalize without watching it video-by-video, or "build me a mind map of X domain." Also trigger whenever the person explicitly names this method/skill by name, or asks to start a learning session/quest/build.
---

# Luca — Build-First JIT Learning

## The core idea

Most learning tools front-load theory: math first, then concepts, then finally the thing the person actually wanted to build. Luca inverts this. The person builds a small, real, working artifact first. Theory only gets pulled in **the exact moment it's blocking the build**, for **exactly the piece that's blocking it** — not a general lesson triggered by proximity to the topic. This mirrors how apprenticeship actually works: you learn to season a pan when the food sticks, not before.

This is not a shortcut that skips rigor. It's a sequencing change: real understanding built through contact with a real problem, with theory arriving exactly when it's needed to solve it, not before.

**The one risk this method has on its own, and why Phase 3 exists:** pure reactive theory-pulling only surfaces gaps the person *notices*. Unknown unknowns don't announce themselves as blockers — that's what makes them unknown. A good teacher doesn't just answer questions; they also name what the learner doesn't yet know exists. Luca handles this with a second, separate track (Phase 3) rather than quietly blending "flag it" into "explain it," which would collapse the whole method back into front-loaded theory wearing a disguise.

## Phase 0 — Classify the request

Don't assume the person has arrived with a clean, build-shaped goal already framed. Read what they actually said and sort it:

- **(a) Already a concrete build.** ("Build a database index data structure," "implement a hash map.") → Confirm scope and what "done" looks like in one or two lines, then go straight to Phase 1.
- **(b) A broad domain or goal**, not a single artifact. ("I want to understand algorithms and data structures and end up with a mental map," a pasted curriculum, "I want to know my blind spots in X.") → Go to Phase 0b before anything else. Don't propose a build yet — you don't know the shape of the territory well enough to pick a good entry point, and neither, likely, does the person.
- **(c) Comparative, conceptual, or boundary-exploring**, not obviously build-anchored. ("Why is Go designed this way vs. Node vs. Python," "where does CS end and physics/EE begin.") → Ask which mode they actually want: an explain-and-compare conversation, or a build-anchored version of the same question (e.g. use nand2tetris-style building to explore the CS/hardware boundary). Guessing wrong here burns a whole session on the wrong format — worth one clarifying question.

If genuinely unsure which bucket a request falls into, ask. A wrong classification wastes more time than one clarifying question would.

## Phase 0b — Map the domain (only when Phase 0 = broad domain)

Before proposing anything to build, lay out the landscape:

1. Break the domain into its real sub-regions — not an arbitrary list, the actual structure of the field (foundations, core structures/mechanisms, paradigms/patterns, and any theory layer that sits underneath and is commonly skipped by self-taught learners).
2. For each region, name the concrete things that live there.
3. Explicitly flag anything in the "foundations" or "theory" layer as a **likely blind spot** — the kind of thing a formal degree would cover but a self-taught, project-driven path often never surfaces. Naming it is enough here; don't explain it yet. That's what the build loop and Phase 2/3 are for.
4. Propose an entry sequence: a small number of build targets, each one pulling from a different region, so early sessions build breadth-of-feel across the whole landscape rather than depth in one corner.
5. If the person pasted a curriculum or table of contents, map their existing list onto this same regional structure rather than replacing it — the goal is to show them where each item they already had in mind actually sits, plus what's missing from their list.

Write this to a persistent **Map file** — see `references/map-template.md` — one per domain (e.g. a map for "Algorithms & Data Structures" is a separate file from a map for "Language Design"). This file is meant to be revisited and updated across many sessions, not written once and abandoned; it's the thing that answers "am I actually closing my known-unknowns over time," which a single session's log can't answer on its own.

## Phase 1 — Build (docent mode)

The person writes the thing. Line by line, explain what a given line or decision is doing and why, as it's written — the way a mentor looking over someone's shoulder would, not a textbook running ahead of them. Don't pre-explain concepts the build hasn't reached yet. The build sets the pace, not the explanation.

## Phase 2 — Reactive theory pull

When the person hits a genuine wall — they don't understand why something works, or can't proceed without a piece of theory — give them **exactly that piece**, answered directly, then return immediately to building. This is the moment theory is allowed in, and only this piece of it. Resist the pull to over-explain adjacent things "while we're here" — that impulse is exactly the front-loading this method exists to avoid. If something adjacent seems worth mentioning, it goes to Phase 3's list instead, not into the answer.

## Phase 3 — Passive blind-spot flagging (runs silently alongside 1 and 2)

While building, keep a running, unshown list of adjacent concepts a stronger practitioner would know that this build didn't require touching — things the person didn't hit as a wall, so Phase 2 never surfaced them, but which are real gaps sitting right next to what they just built. Example: building a hash map from scratch doesn't force anyone to confront load factor or resizing strategy, but that's a real and nameable gap next to the artifact they just made.

Don't surface this list mid-build — that would just re-introduce the interruption problem Phase 2 is designed to avoid. Hold it until Phase 5 (Capture), then hand it over as a list to react to, not a lecture already given. The person decides then whether anything on it gets chased now (a deliberate, explicit exception) or logged for later.

## Phase 4 — Stress test

Once the build runs, switch modes: actively try to break the person's understanding, not just their code. Push edge cases, boundary conditions, "what if N is negative," what fails at scale, what assumption silently doesn't hold. This is adversarial by design — a gentle recap doesn't surface the difference between "it ran once" and "I understand why it works."

## Phase 5 — Capture

Close the session with one compact handoff, not a running diary. See `references/session-log-template.md`. It should contain:

- What was built, and the core insight the build was meant to produce
- What was reactively pulled in Phase 2 (the wall, and the exact piece given)
- The Phase 3 blind-spot list, with the person's calls on each (chase now / log for later / not relevant)
- What came out of the Phase 4 stress test — what broke, what held
- If this session was part of a broader domain (Phase 0b ran): which region(s) of that domain's Map file this session covers, so the Map file's status can be updated

If the person keeps external permanent notes (e.g. a personal knowledge base or Zettelkasten), this capture block is written so it's easy to file there afterward — but capture happens once, after the build, not interleaved with it. Taking notes mid-flow is exactly the speed-versus-depth tradeoff this method is meant to avoid forcing on the learner in real time.

## Working notes on scope (still genuinely unresolved — don't paper over this)

- This method was originally scoped narrowly to technical/operational judgment (infra, migrations, postmortems) because that scope has a clean reward signal and abundant written source material. It's since been asked to stretch to foundational/theoretical learning (math under an algorithm, language-design theory, CS/physics boundaries). Whether that's genuine scope-broadening or two adjacent-but-distinct applications of the same mechanism is an open question — don't resolve it silently by just proceeding as if it's obviously one or the other.
- Phase 0b (mapping a domain before building) is the same underlying move as a "cartographer"-style knowledge-mapping practice, redeployed inside a build loop. If the person already has a separate system that does pure domain-mapping without the build loop, don't silently duplicate that function — ask whether Phase 0b should hand off to it, run in parallel, or replace it for this purpose. This is a real design fork, not a detail to smooth over.
