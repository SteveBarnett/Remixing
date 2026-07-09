---
layout: page
title: Building Great Agent Skills
added: 2026-07-09
updated: 2026-07-09
ai: true
---

Notes from [Building Great Agent Skills: The Missing Manual](https://www.youtube.com/watch?v=UNzCG3lw6O0) and [    writing-great-skills](https://github.com/mattpocock/skills/blob/main/skills/productivity/writing-great-skills/SKILL.md).

## Raw notes

- Trigger: Decide whether a skill should be user-invoked or model-invoked. Matt notes that while model-invoked skills offer more flexibility, they increase context load and introduce unpredictability. User-invoked skills offer more control but require greater cognitive load from the pilot.
    - Pick model-invocation only when the agent must reach the skill on its own, or another skill must. If it only ever fires by hand, make it user-invoked and pay no context load.
    - When user-invoked skills multiply past what you can remember, that piled-up cognitive load is cured by a router skill: one user-invoked skill that names the others and when to reach for each.
- Structure: Organise your skill into two primary units: steps (procedures) and reference (supporting information). To keep the skill.md file minimal, move branching reference material behind context pointers to reduce bloat and maintenance costs.
- Steering: Use leading words—specific terms that pack dense meaning—to influence agent behaviour and guide reasoning traces. Additionally, you can force the agent to perform more "leg work" on specific tasks by breaking complex processes into smaller, individual skills that hide future steps.
- Pruning: Maintain a clean skill set by ensuring a single source of truth, removing "sediment" (irrelevant legacy material), and eliminating "no-ops" (instructions that don't actually change agent behaviour).

### Invocation

Two choices, trading different costs:

- A model-invoked skill keeps a description, so the agent can fire it autonomously and other skills can reach it (you can still type its name too). It contributes to **context load** — the description sits in the window every turn. Mechanics: omit disable-model-invocation, and write a model-facing description with rich trigger phrasing ("Use when the user wants…, mentions…").
- A user-invoked skill strips the description from the agent's reach: only you, typing its name, can invoke it — and no other skill can. Zero context load, but it spends **cognitive load**: you are the index that must remember it exists. Mechanics: set disable-model-invocation: true; the description becomes human-facing — a one-line summary, trigger lists stripped.

### Description

A model-invoked **description** does two jobs — state what the skill is, and list the **branches** that should trigger it. Every word increases **context load**, so a description earns even harder pruning than the body:

- **Front-load the skill's leading word** — the description is where it does its invocation work.
- **One trigger per branch.** Synonyms that rename a single branch are **duplication** — "build features using TDD … asks for test-first development" is one branch written twice. Collapse them; keep only genuinely distinct branches.
- **Cut identity that's already in the body.** Keep the description to triggers, plus any "when another skill needs…" reach clause.

### Information hierarchy

A skill is built from two content types — steps and reference — that mix freely: a skill can be all steps, all reference, or both. The core decision is which to use and where each sits on the information hierarchy, a ladder ranked by how immediately the agent needs the material:

1. In-skill step 
2. In-skill reference
3. External reference 

Push too little down and the top bloats; push too much and you hide material the agent actually needs. That tension is the whole decision.

### When to split

- **By invocation** — split off a **model-invoked** skill when you have a distinct **leading word** that should trigger it on its own, or another skill must reach it. You pay **context load** for the new always-loaded **description**, so that independent reach has to be worth it.
- **By sequence** — split a run of **steps** when the steps still ahead (a step's **post-completion steps**) tempt the agent to rush the one in front of it (**premature completion**). Keeping them out of view encourages the agent to do more **legwork** on the current task.

### Pruning

Keep each meaning in a **single source of truth**: one authoritative place, so changing the behaviour is a one-place edit.

Check every line for **relevance**: does it still bear on what the skill does?

Then hunt **no-ops** sentence by sentence, not just line by line: run the no-op test on each sentence in isolation, and when one fails, delete the whole sentence rather than trim words from it. Be aggressive — most prose that fails should go, not be rewritten.

### Failure modes

Use these to diagnose issues the user may be having with the skill.

- **Premature completion** — ending a step before it's genuinely done, attention slipping to _being done_. Defence, in order: sharpen the completion criterion first (cheap, local); only if it is irreducibly fuzzy _and_ you observe the rush, hide the post-completion steps by splitting (the sequence cut).
- **Duplication** — the same meaning in more than one place. Costs maintenance and tokens, and inflates a meaning's prominence on the ladder past its real rank.
- **Sediment** — stale layers that settle because adding feels safe and removing feels risky. The default fate of any skill without a pruning discipline.
- **Sprawl** — a skill simply too long, even when every line is live and unique. Hurts readability and maintainability and wastes tokens. The cure is the ladder: disclose **reference** behind pointers, and split by **branch** or sequence so each path carries only what it needs.
- **No-op** — a line the model already obeys by default, so you pay load to say nothing. The test: does it change behaviour versus the default? A weak leading word (_be thorough_ when the agent is already thorough-ish) is a no-op; the fix is a stronger word (_relentless_), not a different technique.
- **Negation** — steering by prohibition backfires: _don't think of an elephant_ names the elephant and makes it more available, not less. Prompt the **positive** — state the target behaviour so the banned one is never spoken; keep a prohibition only as a hard guardrail you can't phrase positively, and even then pair it with what to do instead.

