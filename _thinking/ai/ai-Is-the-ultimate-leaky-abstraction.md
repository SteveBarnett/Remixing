---
layout: page
title: AI Is the Ultimate Leaky Abstraction
ai: true
added: 2026-08-10
updated: 2026-08-11
---

Notes from [AI Is the Ultimate Leaky Abstraction](https://www.jonathanbeard.io/blog/2026/06/20/ai-the-ultimate-leaky-abstraction.html)

## Whittled notes

- The Law of Leaky Abstractions: all non-trivial abstractions, to some degree, leak.
- Abstractions are free up until the point they don't work. Then the price, of understanding what it was hiding from you, comes immediately due.
- We all know this feeling from using things that mostly work: maybe the auto mode on a camera, or the battery of a car.
- Generated answers (from LLMs) are an abstraction over reasoning that we cannot ever see.
    - They're probabilistic, not weighted by meaning.
    - They make mistakes where stakes are highest, where the leak is quietest: low-frequency, high-consequence details.
- As we layer bigger and broader abstractions we need to know and understand more, not less, because we still need to be able to pay the price when it becomes due.
- The tool is useful, use it. But/and also keep paying down the understanding for when the leak happens and the price becomes due.

## Gathered notes

- A generated answer is an abstraction over reasoning you never see. It works until it leaks, and when it leaks it hands you a bill for exactly the understanding it let you skip.
- You don’t need to write code to know this feeling; you just need to have leaned on something that mostly works. Think about the auto mode on a camera.
- The abstraction was free right up until the instant it wasn’t, and the price it charged was the exact knowledge it had been saving you from. 
- Joel Spolsky - the Law of Leaky Abstractions, and it has one clause: all non-trivial abstractions, to some degree, leak.
- It hides the complexity and changes when you pay for it.
- Spolsky’s quiet warning was that as our tools climbed higher, the people maintaining the stack had to know more, not less, because every new floor was one more height the leak could fall from.
- the interest compounds hardest in exactly the places the stakes are highest, because those are the places the leak is quietest. ... the model makes those decisions by statistical salience, not by knowing which clause is load-bearing.
- low-frequency, high-consequence detail a fluency-optimized system is most likely to smooth away. 
- it’s useful for the same reason it’s wrong. It discards. 
- The defense isn’t to refuse the tool ... Used well, the payoff is huge. The defense is to keep paying down the understanding before the leak calls it in all at once. 

## Raw notes

- **A generated answer is an abstraction over reasoning you never see. It works until it leaks, and when it leaks it hands you a bill for exactly the understanding it let you skip.**
- An abstraction is a promise that you won’t have to look underneath. Generated answers make that promise too, right up until the moment they break it, and the moment they break it they hand you back a bill for exactly the understanding they let you skip.
- **You don’t need to write code to know this feeling; you just need to have leaned on something that mostly works. Think about the auto mode on a camera.**
- **The abstraction was free right up until the instant it wasn’t, and the price it charged was the exact knowledge it had been saving you from. **
- In 2002 **Joel Spolsky - the Law of Leaky Abstractions, and it has one clause: all non-trivial abstractions, to some degree, leak.**
- The abstraction saved you time while it worked. It never saved you the obligation to understand what it was standing on.
- An abstraction doesn’t erase the complexity beneath it. **It hides the complexity and changes when you pay for it.**
- The bill comes due at the leak, and the currency the leak demands is comprehension
- **Spolsky’s quiet warning was that as our tools climbed higher, the people maintaining the stack had to know more, not less, because every new floor was one more height the leak could fall from.**
- The surface has the texture of competence.
- Intent and reality drift apart in odd ways, and a lot of people make a living in that gap. What made those leaks survivable was inspectability: the substrate underneath was always there to climb down into. This is the difference that matters
- The leak hurt, but it was legible, and legibility is the thing that makes a leak survivable.
- A generated answer withdraws that bargain without telling you. The model’s interior isn’t intricate-but-deterministic engineering; it’s a probabilistic latent space, and the path from any one parameter to any one token can’t be traced by the person leaning on it.
- **the interest compounds hardest in exactly the places the stakes are highest, because those are the places the leak is quietest.**
- This is the leak in its purest form. The abstraction didn’t fail loudly ... It failed silently, in the gap between appearance and behavior, under a condition the prompt never specified and the dev environment never exercised. 
- summarization is compression, and compression is a string of decisions about what’s safe to throw away, and **the model makes those decisions by statistical salience, not by knowing which clause is load-bearing.**
- The one caveat that mattered ... is precisely the **low-frequency, high-consequence detail a fluency-optimized system is most likely to smooth away**. 
- **it’s useful for the same reason it’s wrong. It discards. **
- The failure isn’t that any single answer is false. It’s that the capacity to tell has quietly migrated out of the human and into a system that can’t be inspected. Not incompetence. Not automation. The slow withdrawal of the bargain every abstraction before this one honored: that if you were ever truly forced to, you could descend.
- **The defense isn’t to refuse the tool**, which would be both futile and a little dishonest given how much it actually buys you. **Used well, the payoff is huge.** **The defense is to keep paying down the understanding before the leak calls it in all at once. **
