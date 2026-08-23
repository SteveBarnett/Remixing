---
layout: page
title: "Work: sort-of retro: three weeks of AI"
ai: true
added: 2026-08-23
updated: 2026-08-23
---

This week was a bit tricky to get a hold of because of things happening at work. But, I still have some observations.

## Bit of a summary

- Human expertise is still needed
    - the code doesn't always do what the AI says it does
    - especially for "niche" topics
    - For a11y, this means we still need to read the code
    - AI uses the default/popular/obvious method for testing something, the human adds fallbacks/alternatives
- Still tends to verbose, which makes explanations in particular harder to parse

## What

- Adding one new case: Cards
- Bug hunting and fixing on existing tests
    - blocked status instead of fail or n/a

## What went well

- Back to reading code, applying human a11y expertise
- Refactoring for understandability
- Reviewing PRs is quite fun and feels helpful to the team

## What went badly

- AI output is so verbose
    - make it hard to read, easier to want to skim
    - words in PRs
    - words in Plan mode and explanations and working
    - code is a bit verbose, but not too bad
- Auto mode in Claude Code makes it even easier to abdicate choices and responsibility
- Code not quite doing what the words are saying
    - partly LLM-problem
    - partly a11y SME problem
