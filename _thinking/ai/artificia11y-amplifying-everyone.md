---
layout: page
title: "artificia11y: Amplifying everyone"
added: 2026-07-07
updated: 2026-07-07
ai: true
---

Notes from [artificia11y: Amplifying everyone](https://artificia11y.ds.house/testing/methodology/#run-the-population-test-as-an-eval).

## Whittled notes

- **The models represent the most common, so disability gets treated as an outlier**
- The bias is systemic, structural, from the data and method
    - **It can't be fixed by adding a little disability data and moving on**
- Models get trained on biased model output, amplifying the bias
- **AI tools default to inaccessible markup**
    - Constrain, check, enforcement prompts, accessible component primitives, CI checks
- The two most important ones
    1. **Build on accessible primitives**
    2. **eslint-plugin-jsx-a11y fails CI**
- Feed the system the right knowledge rather than hope it learned it
    - A Knowledge Base
    - **Often more reliable than retraining**
- **Ongoing retests**: on model change, prompt change, new data source

## Gathered notes

- Statistical models push the uncommon to the margins, so disability gets treated as outlier data and left out.
- Representation has to be built in, not assumed
- Models increasingly train on AI output, which can amplify bias and erase the variety disabled users depend on.
    - The data loop can amplify bias when a model trains on its own output or on majority feedback signals.
- Bias against disabled people in AI is structural and predictable, not a rare accident.
    - It comes from the data and method, so you cannot fix it by adding a little disability data and moving on.
- Excluding disability data permits discrimination, but partial inclusion still misses many people, because disability is not one thing.
- AI tools default to inaccessible markup, so constrain and check the generation with enforcement prompts, accessible component primitives, and CI checks.
- A curated knowledge base is a feedback loop you control, and often more reliable than retraining.
- Two moves do most of the work.
    - The first is to have the AI build on accessible component primitives not have to get them right from scratch.
    - The second is to set eslint-plugin-jsx-a11y to error in CI so a broken pattern cannot merge.
- One practical loop is to feed the system the right knowledge rather than hope it learned it.
- Run the population test as an eval: track the aggregate pass rate over time
- Tie a retest to a model change, a prompt change, or a new data source

## Raw notes

### Training data

- Statistical models push the uncommon to the margins, so disability gets treated as outlier data and left out.
- Representation has to be built in, not assumed
- Models increasingly train on AI output, which can amplify bias and erase the variety disabled users depend on.

### Bias and representation

- Bias against disabled people in AI is structural and predictable, not a rare accident.
- It comes from the data and method, so you cannot fix it by adding a little disability data and moving on.
- Excluding disability data permits discrimination, but partial inclusion still misses many people, because disability is not one thing. 

### Feedback loops

- AI tools default to inaccessible markup, so constrain and check the generation with enforcement prompts, accessible component primitives, and CI checks.
- The data loop can amplify bias when a model trains on its own output or on majority feedback signals.
- A curated knowledge base is a feedback loop you control, and often more reliable than retraining.
- The cheapest place to catch an accessibility problem is while the code is being written, including when an AI tool writes it. A reusable enforcement prompt can make an AI coding assistant check keyboard access, focus, and labeling as it generates, and report what it changed. In continuous integration, a scanner can file issues, and a workflow can track remediation over time. None of this replaces human and user testing, but it stops obvious regressions early. 
- Two moves do most of the work. 
    - The first is to have the AI build on accessible component primitives not have to get them right from scratch.
    - The second is to set eslint-plugin-jsx-a11y to error in CI so a broken pattern cannot merge. 
- One practical loop is to feed the system the right knowledge rather than hope it learned it.

### Testing methodology

- Run the population test as an eval
    - The AI-engineering name for sampling that population is an eval. You assemble a fixed set of prompts, run each one through the real rendering pipeline, score the output against accessibility checks, and report an aggregate pass rate rather than a single pass or fail. That pass rate is the metric you track over time. Because output is probabilistic, one number across many prompts tells you far more than one green check on one answer.
- A model change, a prompt change, or a new data source can regress accessibility with no change to the code you would normally re-audit. So testing repeats. Tie a re-test to those triggers, as described in The feedback loop.
