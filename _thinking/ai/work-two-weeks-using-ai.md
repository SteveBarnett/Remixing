---
layout: page
title: "Work: sort-of retro: two weeks heavily using AI"
ai: true
added: 2026-08-16
updated: 2026-08-16
---

I've not spent two weeks using Claude Code pretty much all day every day for work. I did [a mini-retro for week one](/thinking/ai/work-one-week-heavily-using-ai/), and here's one for week two.

## Bit of a summary

- They typing part is sped up considerably
- The reviewing part tends to be slower, require more careful checking
    - We're deferring code reviews as each PR is already big
        - **Are the a11y checks actually doing what they say they're doing? This needs an SME.**
- **It makes the feasible part appear much bigger, backgrounding desirable and viable**
- **When there's a user-question (in a bigger process), there's a pull towards the one that lets AI do it all ("Recommended")**
- **The various pulls combine, intersect with, and compound each other**
- **The "Make me a new X, like A, B, C" works well, but/and carries forward all the mistakes we haven't spotted yet**
- **Don't feel as much ownership of the output**

---

## What

- Generating evals for more complex cases
- Making lots of PRs
- Reviewing lots of PRs
- Discussing a bigger change, using Claude to audit and make a plan

## What went well

- Feels great to be moving fast. It's definitely faster than without it. "Generate a new one for X, follow the pattern of the others" works well.
- Something we're trying: doing code, technical, reviews separately.

## What went badly

- The pull to multitasking
    - Bigger prompts / asks mean waiting for the model to respond.
    - It becomes jaggedy because it asks along the way ("Run this bash command?" and "Edit this file?" and so on).
    - Or you say set it to auto and most things will be an automatic yes. But then the work moves to more time in reviewing.
- The pull to be ever more productive
    - The higher speed of output means higher quantity of output
    - There's pressure to do lots more, just because you can
    - It foregrounds and highlights the quantity, backgrounding quality and whether it should be done at all
        - **It loudly makes more things seem feasible, backgrounding desirable and viable**
    - Skimming it, so the understanding is shallower
    - The hype adds implied pressure and expectation to be vastly more productive
- Narrowing of options and thinking
    - When doing big plans with multiple paths, several options are offered. One is "Recommended", and the pull to just say yes to that one is strong.
        - Often there are three options, something like: do this change; I'll do this change myself; stop everything. The last one feel like a pain, starting over, so there's a pull to do one of the first two. And there's a pull to let the AI do more work.
- Review fatigue
    - There's more to review, more quickly
    - Reviewing in-depth "slows you down"
    - But/and skimming it means risking low quality
- Answers can be very verbose
    - We have a change we were thinking of making across the whole code base. We asked Claude to audit the code and make a plan for the change. It make a comprehensive plan, but/and it was really wordy.
- Don't feel as much ownership of the output
    - Sometimes don't check as carefully as I should
    - The text chunks in particular are verbose and read well with a cursory skim
- Hit my usage limit
    - Puts the breaks of hard
    - Since we're relying on to generate stuff
- Problems we haven't spotted yet get spread through the whole codebase
    - And new a PR to tidy up
- Everything, everywhere, all at once
    - **These combine and intersect with and compound each other**
