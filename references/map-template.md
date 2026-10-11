# Bottega templates

Three files per workspace. MAP.md is the one that matters most: it's the live plan, the
progress record, and the resume point, all in one place so nothing drifts between files.

---

## `bottega/<topic>/MAP.md`

```markdown
# [Topic]: Luca map

**Goal (learner's words):** "[verbatim]"
**Studying:** topic | codebase · **Target rung:** Scout (default) · **Stakes:** [codebases only]
**Created:** [date] · **Last updated:** [date]

## Level contract
- **Target:** Scout (aka Orient)
- **This gives you:** [e.g. what each region is for, what it assumes, where it fits]
- **This won't give you:** [e.g. writing it from memory in two weeks]
- **Next rung would take:** [e.g. one more stop per item, writing from a blank file]

Ladder: Scout (Orient) → Wield (Apply) → Reforge (Rebuild) → Vouch (Own)
Status: 🔴 not touched · 🧩 flagged, not yet chased · 🟡 touched, below target ·
🟢 [rung] reached, with evidence

## Map

[Mermaid diagram when the structure matters]

### 0. Foundations (the layer project-driven learning tends to skip)
- [Item]: 🧩
- **Questions worth asking:** [1–2 questions a practitioner would ask here]

### 1. [Region]
- [Item]: 🟢 Scout (predicted all three outputs correctly) · next: Wield
- [Item]: 🔴
- **Questions worth asking:** ...

[As many regions as the real structure needs. Don't force every domain into one shape.]

## Route
*Level contract applies. Tick or defer every item before leaving a stop.*

- [x] **Stop 1: [name]** (Scout, ~15 min)
  - [x] [item]
  - [x] [item]
- [ ] **Stop 2: [name]** (Scout, ~15 min)
  - [ ] [item]
  - [ ] [item]: deferred, [reason]

## Click lines
- [date] [item]: confused by [X]; clicked when [Y].
- [date] [item]: predicted [A], got [B], because [C].

**Next recall:** [item] ([rung studied at])

## Open blind spots (🧩)
- [item]: [why it's adjacent to what was built]

## History
| Date | Stops | Takeaway |
|---|---|---|
| | | |
```

---

## `bottega/<topic>/TODO.md`

Shared by the learner and Luca. The learner adds lines freely; Luca adds parked questions and
TODO comments found in code. Keep one list per topic so a TODO never lives in two places.

```markdown
# TODO: [Topic]

- [ ] [The learner's own TODO]
- [ ] [Parked question from a session] (from stop 3, [date])
- [ ] [TODO comment found in code] (`path/to/file.c:42`)
```

---

## `bottega/README.md`

Luca's own README. The repository's top-level README is never touched.

```markdown
# Bottega

Luca's workshop: learning maps and experiments. Each topic folder has a MAP.md (the plan and
progress), a TODO.md, and a lab/ of runnable experiments.

| Topic | Target rung | Last session | Next |
|---|---|---|---|
| [topic](topic/MAP.md) | Scout | [date] | Stop 3: [name] |

**To resume:** open this README, then the topic's MAP.md and TODO.md.
```
