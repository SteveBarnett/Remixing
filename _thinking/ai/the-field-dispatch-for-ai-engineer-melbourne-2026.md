---
layout: page
title: The Field Dispatch for AI Engineer Melbourne 2026
ai: true
added: 2026-07-21
updated: 2026-07-21
---

My notes from [The Field Dispatch — AI Engineer Melbourne 2026](https://fieldreports.webdirections.org/ai-engineer-melbourne-2026/)

## Gathered notes

- The harness beats the model
    - use checklists
    - re-read the goal every few steps
    - force verification after each meaningful step
- Match the model to the task
- Where memory should live (files, platforms, model) is still being discussed
- Spec, docs, as source of truth
- Evals are the new tests
    - Eval on business goals, not proxies
    - What could be deterministic rather than an LLM judge?
    - Who reviews and (re)aligns the judge?
    - (The recursive problem of needing evals to judge your evals)

## Raw notes

### THE SIX THEMES

1. The harness beats the model
    - The base model is a commodity; the moat is routing, context, cascades — and knowing when a smaller model (or none) does the job.
2. Context isn't memory
    - Agents forget everything, and a bigger window doesn't fix it. Where memory should live — files, platforms, or the model itself — split the speakers three ways. Honestly unsolved.
3. Evals are the new tests
    - You can't ship non-deterministic systems on vibes. Deterministic checks first, judges on a leash, traces as the shared language.
4. Spec is the source
    - “We've been backing up the wrong files.” When code is regenerable, what do we keep — the spec, the loop, or the why? One room, one afternoon, three answers.
5. The economics broke
    - Token spend is engineering now. Prices per capability collapse; total spend rises anyway — both true at once, and the same cautionary tale surfaced in two rooms.
6. The org is the bottleneck
    - The limiting factor is organisations — governance shape, boardroom miscalibration, and engineers afraid of becoming junior again.

### 01 · The harness beats the model — The Field Dispatch

#### KEY QUESTIONS TO DISCUSS WITH YOUR TEAM

- ENGINEER: Do you know the cost per task and failure rate of the workflow you run most? If you swapped in a model a tier down tomorrow, what would catch its failures?
- Team lead: Where in your process would “why this model for this task?” actually get asked — design review, PR template, eval sign-off? Right now, is it asked anywhere?
- Org leader: Is your model spend a line item someone owns, or a surprise at the end of the quarter?
- For the whole team: Cameron says harnesses are overbuilt; Tirupathi says the harness is the moat. Run the argument for your own stack: which failure mode are you closer to — orchestration you don't need, or defaults you haven't examined?

### 02 · Context isn't memory — The Field Dispatch

How to build real memory is the field's most honestly unsolved problem.

Three live disagreements, honestly held:

- where memory belongs (files, a managed platform, or inside the model itself — the speakers split three ways);
- whether bigger contexts will quietly dissolve the problem anyway (even the sceptics are still growing them);
- and whether persistence is even the goal — Roy argues for forgetting by design when memory health drops, while others want the agent's “soul on disk.”

What nobody claimed is that it's solved.

#### Next steps

- Engineers: Steal the harness moves that beat big contexts: checklists, make the agent re-read its goal every few steps, force verification after each meaningful step (Li). Gate every memory write, and timestamp everything (Roy).
- Key takeaway: Stop buying a vector database as “memory” by default. Costa: “you're basically adopting SAP.” Tirupathi's stack: plain files plus full-text search covers most of it; add a graph only for entity-heavy queries.

#### Key questions to discuss with your team

- Engineer: What does your agent re-read to stay on goal, and how often? Li's finding: checklists and forced re-reads beat a million-token window.
- For the whole team: Files, a platform, or inside the model — where do you think agent memory belongs, and what evidence would change your mind? The speakers split three ways; your team probably will too.

### 03 · Evals are the new tests — The Field Dispatch

Key takeaway: Stop shipping on the one-line judge. “Rate this 1–10 for helpfulness” isn't an eval — it's the fitness function your self-improving agent will learn to game (Dixit).

#### Key questions to discuss with your team

- Engineer: What in your current eval could be a checksum, a schema check, or a totals comparison instead of a judge call? That's free compute you're paying a model for.
- Engineer: If your agent optimised hard against your current eval, what would it game first? That's Dixit's paradox pointed at your own system.
- Team lead: Who reviews your judge? When was it last aligned against human labels — and has anything changed since?
- Org leader: Which business metric do your evals actually move? If the answer is a compliance score, you're optimising a proxy.
- Org leader: Do you know your testing-and-evals token bill per developer? Orgs are budgeting six figures a year per head out there — knowingly or not.
