---
layout: page
title: "Work: sort-of retro retro: heavily using AI"
ai: true
added: 2026-09-16
updated: 2026-09-16
---

Over the past few weeks I've been using AI quite heavily. This was for generating automated tests (some unit tests, some E2E tests using Playwright) for testing accessibility.

Every week, I did a little mini-retro for myself. Here are some of the points that came up.
## Ups

- Claude Code made writing code (for the tests) much faster, with generally good quality output.
    - In particular for generating new tests based on old tests.

## Downs

- It was good at generating the default/popular/obvious methods for testing something, but we needed to add many fallbacks/alternatives
- Basing new tests on old ones speeds things up, but errors we hadn't spotted yet carried forward.
- It struggled for our niche, accessibility topic in terms of meaning.
    - Some tests didn't do quite what they said they did. And/or they didn't test the right thing.
- Relatedly, reviewing code was slower than reviewing human-written code.
- The output tends towards verbose, even with some steering.
    - Each Pull Request tended towards the large size.
    - Each bit of code tended towards more lines than fewer.
    - Explanations in comments in the code, or in Plan mode, are harder to parse.
    - The verbosity problem compounded pretty quickly as we proceeded.
- I didn't feel as much ownership or interest in the code.

## Pulls

- I felt a psychological effect on myself. An addiction-like pull similar to a smartphone.
    - Something like: because it's there, you "should" be using it more. Do-maxxing, if you will.
    - Using AI to generate things makes the feasible part appear much bigger, backgrounding the desirable and viable parts.
- When there's a user-question (in a bigger process), there's a pull towards the one that lets AI do it all ("Recommended")
- The various pulls combine, intersect with, and compound each other
