---
layout: page
title: 'Can AI “Scheme”? (Nope.) | AI Reality Check'
added: 2026-04-06
updated: 2026-04-06
ai: true
---

Notes from Cal Newport's [Can AI “Scheme”? (Nope.) – AI Reality Check](https://www.youtube.com/watch?v=Q_zRYOwlVFU).

## Gathered notes

- LLMs finish the story that a text input starts.
- This includes plans. LLMs generate a plausible story of a plan.
- Agents built on LLMs are unreliable and make mistakes because they are following the story of a plan, not a plan.
- The story of a plan doesn't involve thinking, evaluation, or validation.

### Coding agents are an exception / proof of the rule

- the options for the plan are limited, restricted;
- the examples to draw from are well-documented;
- the agent can check the steps (does the code compile, pass tests, etc).

### No thinking or feeling

- News reports of deception, blackmail, scheming, make more sense with this context: the LLM is completing a story started by a text input.
- There are no intentions in auto-regressive token production.

### Longer responses

- Longer responses are auto-regression:
    - user prompts with input text
    - LLM generates a one word response
    - response is added to the input text
    - LLM uses new input text to generate a one word reponse

## Raw notes

- The digital brain that powers an agent is almost always an LLM.
- The agent sends prompts to the LLM, the LLM responds with a plan, the agent runs the plan.
- **Building agents on LLMs is fundamentally flawed.**
- Overall, **LLMs finish the story that the text input started.**
- LLMs are trained to "think" the input text is part of a larger text that already exists, and it guesses the next word or part of word.
- **Longer LLM responses are (a behind-the-scenes) auto-regression: prompt and get one word response, add that to the existing input, prompt (the same LLM) again.**
- That includes writing plans. No thinking, no evaluation of rule or steps, no checking against restrictions, no checking against goals, no scheming. **LLMs finish the story of a plan.**
- **They are unreliable and make mistakes because they're following the story of a plan (that seems coherent, plausible), not a plan.** It's a fundamental mismatch.
- **The (famous) stories of AI deception and blackmail make more sense when we think about them as LLMs trying to complete a story.**
- **Prompts that include "you are an AI" are much more likely to get sci-fi answers.**
- **There are no intentions in auto-regressive token production.**
- Coding agents are the exception that proves the rule. They're the best case scenario because: 
    - the options for the plan are limited, restricted;
    - the examples to draw from are well-documented (in particular Q&A format;
    - the agent program can check steps itself (which isn't possible for most other agents) - does the code compile, pass tests, etc.

### Conclusion

- LLMs shouldn't be used on their own to plan for autonomous action. They're not good at that. Except for coding or when using something other than an LLM.
