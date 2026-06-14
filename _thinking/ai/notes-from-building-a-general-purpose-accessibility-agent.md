---
layout: page
title: Notes from 'Building a general-purpose accessibility agent'
ai: true
added: 2026-06-14
updated: 2026-06-14
---

Notes from [Building a general-purpose accessibility agent—and what we learned in the process - The GitHub Blog](https://github.blog/ai-and-ml/github-copilot/building-a-general-purpose-accessibility-agent-and-what-we-learned-in-the-process/)

## Whittled notes

- Vague SKILL files aren't enough. Use your own detailed data of issues and fixes.
- Don't use it for complex code. Refer to a human instead.
- Don't use it for high-risk patterns.
- Reduce the bias to action. Watch for the tendency to prefer providing solution, rather than deferring.
- Use pull request reviewer sentiment as a signal for where the agent needs work.

## Gathered notes

- Much like with any other specialized domain area, vague instructions in a skill file won’t cut it. Telling an LLM to “use accessibility best practices” with a short list of examples won’t work well.
- So, I enthusiastically recommend investing in manually cataloging and remediating accessibility issues. After some progress, this data can be incorporated into the agent.
- Evaluate code complexity
    - If the score passes a set threshold, the agent is instructed to not execute code changes. Instead, it will inform the person using the LLM that they should reach out to the accessibility team to consult on what they are attempting to do.
- Identify high-risk patterns
- Reduce bias to action
    - We had to create anti-gaming instructions to prevent the LLM from creating sneaky ways to get around its instructions to not generate code when human expertise is needed. This prevented it from violating its own intervention instructions.
- We periodically perform manual review of agent output to determine its accuracy and efficacy. In addition, we have tooling in place to capture pull request reviewer sentiment. Both serve as strong signals for areas where the agent needs better instruction, as well as new resources and skills.

## Raw notes

1. Providing engineers with reliable, just-in-time answers to accessibility questions in the GitHub Copilot CLI and the Copilot VS Code integration.
2. Catching and automatically remediating simple, objective accessibility issues before they go to production.

For purpose number two, the accessibility agent is set to automatically evaluate changes that modify our front-end code.

The accessibility agent is not a “silver bullet” that can automatically address every hypothetical scenario. Understanding, honoring, and socializing this better helps set the agent’s scope of responsibility. This sped up the experiment’s launch, leading to more buy-in for the effort.

**Much like with any other specialized domain area, vague instructions in a skill file won’t cut it. Telling an LLM to “use accessibility best practices” with a short list of examples won’t work well.**

When generating code, LLMs have an unfortunate bias towards producing accessibility antipatterns since every major LLM currently available is trained on decades of inaccessible code.

To counteract this, the agent needs better content to draw from.

**So, I enthusiastically recommend investing in manually cataloging and remediating accessibility issues. After some progress, this data can be incorporated into the agent.**

a general-purpose accessibility agent can consume a ton of tokens when it performs work. This has three negative outcomes:

- An increased amount of unreliable output
- Slower response times
- Increased operational costs

Use sub-agents

The first sub-agent acts as a passive reviewer and researcher.
The second sub-agent acts as an active implementer.

The concern of using sub-agents to increase the speed of the LLM’s reply is counterbalanced by our need for its results to be accurate. We found that compelling the agent to execute its sub-agent instructions in a fixed order was key.

The two schema templates are:

- Reviewer template schema: This focuses on what to audit, and how to find applicable information about it.
- Implementer template schema: This focuses on what to fix and how to fix it.

Without the schema files in place, the agents would all attempt to arbitrarily communicate with each other. This would create increased token expenditure, undesirable hallucinations, unnecessary code changes, and difficult-to-impossible behavior for agent auditing purposes.

Another vital aspect of creating the accessibility agent is understanding areas where agents can fall short.

Here’s what we did to accommodate the agent’s limitations:

**Evaluate code complexity**

- **If the score passes a set threshold, the agent is instructed to not execute code changes.** Instead, it will inform the person using the LLM that they should reach out to the accessibility team to consult on what they are attempting to do.

**Identify high-risk patterns**

It is a subtle thing to understand, but know that it is entirely possible to have code that passes automated accessibility checks, yet is functionally unusable.

- Not prohibiting high-risk patterns and high-complexity code environments would lead to unnecessary demands of everyone’s time to readdress, and also represents reputational risk for the accessibility team. We avoid this by shutting off the LLMs capability to go down this pathway.

**Reduce bias to action**
    - We had to create anti-gaming instructions to prevent the LLM from creating sneaky ways to get around its instructions to not generate code when human expertise is needed. This prevented it from violating its own intervention instructions.

**We had to create anti-gaming instructions to prevent the LLM from creating sneaky ways to get around its instructions to not generate code when human expertise is needed. This prevented it from violating its own intervention instructions.**

Know that programmatically determinable issues don’t cover everything

Manually evaluate agent output and adjust things that aren’t working as expected

**We periodically perform manual review of agent output to determine its accuracy and efficacy. In addition, we have tooling in place to capture pull request reviewer sentiment. Both serve as strong signals for areas where the agent needs better instruction, as well as new resources and skills.**

To recap, we learned that the agent is:

- Used to aid and augment existing accessibility efforts, not to replace them.
- Significantly more effective when trained on manually audited and remediated accessibility issues for your specific experience.
- Far more efficient with token consumption when utilizing sub-agents.
- More accurate and effective when executing instructions in a methodical, linear fashion.
- More consistent when set to use preformatted templates to pass information around.
- Set to understand its limitations and route people to alternative support systems.
- Improved when its output is periodically reviewed to identify areas it needs better instruction.
