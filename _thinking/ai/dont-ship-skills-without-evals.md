---
layout: page
title: Don't Ship Skills Without Evals
ai: true
added: 2026-07-21
updated: 2026-07-21
---

Notes from [Don't Ship Skills Without Evals — Philipp Schmid, Google DeepMind](https://www.youtube.com/watch?v=0vphxNt4wyk).

## Notes-for-self

- We can eval our skill, a bit
- Do we want a guide for how ppl can eval it in their context
    - We can't test all the setups, stack, and interaction with other skills
- Where does our SKILL actually run?
    - People are writing React more than HTML
- People are maintaining code and fixing code more than writing new code?

## Gathered notes

- **Write a good description**
    - Include the what (capability) and the when (trigger)
    - Use an active directive, not a passive explanation: "Always use" not "is recommended"
- **Write a good skill**
    - Have the main SKILL.md under 500 lines
    - Under 200 lines can still get good results
    - Remove No-Ops: things that don't alter the agents behaviour
    - Describe goals and constraints, not the step-by-step
        - Use scripts for step-by-step!
- **Do good evals**
    - Start with a small (10-20) set of prompts
    - Include negative tests: when the skill should not trigger
    - Grade the outcome, not the path
    - Use a clean workspace for every test case
    - Eval across agent frameworks
    - Against code, regex can cover a lot of the work

## Raw notes

[SkillsBench: Benchmarking How Well Skills Work Across Diverse Tasks](https://www.skillsbench.ai/)

- Bad skills don't crash; they quietly corrupt outputs
- The hidden reliability gap: agents we use vs agents we build

### Capability skills

- Teach models what they can't consistently do yet
- Temporary (retire as models improve)
- Evals tell you when to retire a skill

### Preference Skills

- Encode team workflows and conventions
- Durable (must match team process)
- Evals protect against workflow regressions

### From SkillsBench stats

- Human-authored perform better than AI-generated
- Main SKILL.md 200-500 lines is the sweet spot (22% lift)
    - But <200 lines still good (19% lift)

### User-invoked skills can be very powerful

- The trigger mechanism causes 50% of all skill failures
    - Include the what (capability) and the when (trigger) in the description
    - Active directive, not passive explanation
- Describe what you want, not the step-by-step path to get there
    - Goals and constraints
    - Step-by-step means use a script instead of a skill
- Prevent trigger hijacking by defining when skills must NOT fire
    - Track false-positive triggers in evals
- Test early with 10-20 prompts
    - Mix of happy path and not
- Remove No-Ops: things that don't alter the agents behaviour
    - If nothing changes when the line's removed, remove it!
- Retire skills when models catch up

### Prompt scheme

- id
- prompt
- should_trigger
- expected_checks

### Fast Regex checks (Skip LLM calls)

- Against code, regex can cover a lot of the work

### LLM-as-Judge

- For qualitative evaluation: style, formatting, tone, instruction adherence

Require proof of positive Skill Lift before merging the PR

### 10 best practices for skill evals

1. Start with the skill description
    - Trigger problems cause 50% of failures. A vague description causes missed triggers or false fires. Fix description first.
2. Write directives over passive info
    - Models follow instructions better than inferring implications. "Always use" not "is recommended"
3. Include negative tests
    - Add prompts where the skill should NOT trigger to prevent a skills with broad keywords from hijacking every request.
4. Start small, extend from failures
    - Begin with 10-20 prompts. Don't be exhaustive upfront. Every user-reported bug becomes a new test case.
5. Grade outcomes over paths
    - Agents take unexpected routes to correct answers. Grade code execution, API correctness, and goals. Avoid checking file read sequences.
6. Isolate each run
    - Use a clean workspace en for every test case. Context bleeding between runs masks real failures.
7. Run 3-5 trials per case
    - Behaviour is probabilistic. Look at pass^k (consistency) rather than pass@k (peak luck)
8. Test across harnesses
    - Skills behave differently across agent frameworks. Eval in each target environment
.git9. Graduate your evals
    - Capability evals start at low pass rates. One they hit ~100%, graduate them into regression evals that prevent backsliding.
10. Detect skill retirement
    - Run evals with skill unloaded. If they still pass, the base model absorbed the value. Retire the skill to free up context.


