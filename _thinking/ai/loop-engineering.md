---
layout: page
title: Loop Engineering
added: 2026-07-09
updated: 2026-07-09
ai: true
---

Notes from [AddyOsmani.com - Loop Engineering](https://addyosmani.com/blog/loop-engineering/).

## Gathered notes

1. Automations, on a schedule. E.g. discovery and triage.
2. Worktrees, to avoid conflicts.
3. Skills. 
4. Plugins and connectors to existing tools.
5. Sub-agents, so one does and one checks.

Memory, a state file. History, where to start next time. Maybe a markdown file. The agent forgets, the repo doesn't.

Three problems that stay, and are harder:

1. Verification. Your job is to ship code you confirmed works.
2. Comprehension Debt. Your understanding still rots if you allow it.
3. Cognitive Surrender. The comfortable posture is the dangerous one.

## Raw notes

Loop engineering is replacing yourself as the person who prompts the agent. You design the system that does it instead. ... I believe this may be the future of how we work with coding agents. However, its still early, I’m skeptical and you absolutely have to be careful about token costs ...

For like two years the way you got something out of a coding agent was you wrote a good prompt and shared enough context.

Now you build a small system that finds the work, hands it out, checks it, writes down what is done and then decides the next thing, and you let that system poke the agents instead of you.

The five pieces, and then notes

A loop needs five things and then one place to remember stuff. Let me list it first and then map it.

1. **Automations that go off on a schedule and do discovery and triage by themselves.**
2. Worktrees so two agents working in paralell dont step on each other.
3. **Skills to write down the project knowledge the agent would otherwise just guess.**
4. **Plugins and connectors to plug the agent into the tools you already use.**
5. **Sub-agents so one of them has the idea and a different one checks it.**

Then the sixth thing, the memory. A markdown file, or a Linear board, anything that lives outside the single conversation and holds what’s done and what is next. .... The agent forgets, the repo doesn't.

Automations are what make a loop an actual loop and not just one run you did once.

... you define an autonomous task, you give it a cadence, and the findings come to you so you are not the one going around checking. ...

The state file is the spine of the whole thing, it remembers what got tried, what passed, what is still open, so tomorrow morning the run picks up where today stopped.

three problems actually get sharper as the loop gets better, not easier.

1. Verification is still on you. your job is to ship code you confirmed works.
2. Your understanding still rots if you allow it. comprehension debt
3. the comfortable posture is the dangerous one. cognitive surrender.

Build the loop. But build it like someone who intends to stay the engineer, not just the person who presses go.