---
layout: page
title: "Work: sort-of retro retro: heavily using AI"
ai: true
added: 2026-09-16
updated: 2026-09-16
---

Over the past few weeks I used AI quite heavily. This was for generating automated tests (some unit tests, some E2E tests using Playwright) for testing accessibility.

Every week, I did a little mini-retro for myself. Here are some of the points that came up.

## Ups

- Claude Code made writing code (for the tests) much faster, with generally good quality output.
    - In particular for generating new tests based on old tests.

## Downs

- It was good at generating the default/popular/obvious methods for testing something, but we needed to add many fallbacks/alternatives
- Errors we hadn't spotted yet carried forward (when generating new tests based on old tests).
- It struggled with the specifics for accessibility.
    - Some tests didn't do quite what they said they did. And/or they didn't test the right thing.
- Relatedly, reviewing code was slower than reviewing human-written code.
- The output tended towards verbose, even with some steering.
    - Each Pull Request tended to be large.
    - Each bit of code tended towards more lines than fewer.
    - Explanations in comments in the code, or in Plan mode, were harder to parse.
    - The verbosity problem compounded pretty quickly as we proceeded.
- I didn't feel as much ownership or interest in the code.

## Pulls

- I felt a psychological effect. An addiction-like pull similar to a smartphone.
    - Something like: because it's there, I "should" be using it more. Do-maxxing, if you will.
    - Using AI to generate things made the feasible part appear much bigger, backgrounding the desirable and viable parts.
- When there was a user-question (in a bigger process) with options, there was a pull towards just letting AI do it all ("Recommended").
- The various pulls combines, intersected with, and compounded each other.
