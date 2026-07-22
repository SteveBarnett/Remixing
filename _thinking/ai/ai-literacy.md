---
layout: page
title: AI Literacy
ai: true
added: 2026-07-21
updated: 2026-07-21
---

## Gathered notes

- AI tools can be useful
- AI tools fail in known and specific ways
- Knowing the ways they fail is key to using the tools well
  - What it can do, what it can't
  - Choose where, when, and how to use automation
- "AI in the loop", not "human in the loop"; Centaur (a person assisted by a machine), not Reverse centaur (a person assisting a machine). 
- Failure modes
  - Hallucination
    - Truth
    - generating false information, presenting as true
    - Ubiquity of hallucinations, avoid LLMs for generating info
    - Check everything it produces, in fine detail.
        - Check for accuracy and consistency.
        - Be an expert in the domain you’re using it for.
        - AI is know to be inconsistent and inaccurate, to contain errors and omissions.
  - Specifics
  - Cognitive decline
  - Privacy
    - Privacy risks, opt out of user-content training, or locally host
  - expressing
    - the information you put is not private
    - researchers are finding new ways to leak data
    - user inputs are used to train chatbots
  - asking
    - AI is notoriously sycophantic
      - Sycophancy - use them to falsify rather than validate
    - exacerbates providing false information: providing what the user wants to hear, not what is true
    - you can pitch a wrong idea, and the LLM will egg you on
    - it is likely that (social) sycophancy worsen problem with, for example relationships 
      - perceived they were more right, less likely to try and work things out
- Consider whether the task involves personal relationships or high-stakes decisions
- You consider what AI does well and where it struggles
  - Good at: generating options, structure
  - Bad at: nuance and tone, specific facts, being concise
- You break complex tasks into smaller steps for the AI to follow 
  - Guiding AI through a process step by step helps you maintain control and catch issues early rather than at the end.
- Showing AI concrete examples of your expectations communicates more than abstract descriptions ever could.
- Verifying important information AI provides protects you from confidently sharing something incorrect.
- Being thoughtful about the data and context you provide protects privacy and helps you use AI responsibly.
- Stick close to reality, not hypotheticals or maximalist stances
- There are no ethical AI companies, only a hierarchy of harm
  - Environmental Impact
  - Labor Exploitation
  - Mental Health Exploitation
  - Truth About Capabilities
  - Safety Theater vs. Safety Work
  - Community Harm
  - Corporate Transparency
- These systems consume an unfathomable amount of data, land, energy, labour, and water.
- AI frames the process as an obstacle.
    - But the process is where we learn, where we decide.
    - It’s the hard part, where we’re challenged, where we ask for help.
    - Using AI to fix things means we don’t learn, and don’t want to learn, to avoid making those mistakes in the first place
    - Our skills atrophy
- Call out the Hype
- Advocate for the Rights of Workers
  - Unionise and organise
- Reduce your dependence on Big Tech
- Don’t Believe The Hype.
  - Be a sceptic. Ask lots of questions using a critical lens. In particular: ask for the details and specifics.
  - Read calls to use AI as a sales pitch. 
  - AI can’t do your job, but an AI salesperson (or an AI!) can convince your boss it can.
  - Replacing people with AI is a marketing strategy, not a production strategy.
- offer good, time-tested, alternatives.
- Notice the humans workers behind-the-scenes of AI
  - Follow the chain and see how it all comes down to humans: the training data, the Reinforcement Learning from Human Feedback.
- Be wary of anthropomorphising. AIs are not sentient or conscious.
  - They can’t choose or select or decide or interpret.
  - They can’t have empathy or personal interest: these things require subjective experience and human connection.
- Have an AI policy at work.
  - Decide when it’s appropriate and not appropriate to use AI.
- Prefer local, smaller, models to mitigate the harms of large cloud ones.
- Start with the problem rather than AI as the solution.
    - Social and systemic problems rarely have technology solutions.
    - Problems are often best understood looking at the wider context and systems.
- Put the burden of proof of effectiveness on the AI systems.
    - Clarify how the results of adding AI will be measured, and what will happen afterwards.
    - Extraordinary claims require extraordinary proof.
- Use a human-centred, people-first, approach.
    - Remember that AI provides information and knowledge, not wisdom. Wisdom requires broad context, weighing options, working with paradoxes and “it depends”.
- Object to the current harms
    - Ecological, environmental, harm of the water and power use.
    - Ethical harm to the underpaid and traumatised gig workers on the training data and doing Reinforcement Learning from Human Feedback. Psychological harm and deadly harm, such as AI-assisted suicides.
    - Financial harm from the hundreds of billions of dollar investments with little or no return.
- Critique the inputs
    - Mostly Western ideas and approaches.
    - Mostly discriminatory data, replicating the biases and power imbalances of the world.
    - Training data is only the recorded data of the world. Much of human experience isn’t and can’t be recorded.
- Critique the outputs
  - Mode amplification. The most frequent data points are represented as the one true answer.
    - Confabulation and “hallucinations.” Confident bullshitting, made-up things presented as facts.
    - The Wikipedia version of reality. The style of the output is the rational discourse of the educated classes of society.
- Show how reliance on AI can devalue humans and lived experience
    - Atrophying skills of critical thinking and analysis.
        - We learn by actively applied effort.
        - Devaluing human skills such as contextual awareness and conflict resolution.
    - Presenting the process as more important than the product.
        - Thinking and understanding happens as we write, draw, code.
    - Narrowing our curiosity.
        - When we start with AI as a solution, we look for problems that AI can solve.

## Raw notes

Here are two section outlines — one for the failure-modes content (works for any of the three headings you listed), one for the guidelines/harm-reduction content (works for either heading).

### Section 1: AI Failure Modes (covers "Where AI Actually Fails" / "Common Failure Modes and How to Catch Them" / "Frontend Risks")

**1. Opening framing**
- One or two sentences: AI tools are useful *and* fail in predictable, specific ways — this section is about recognizing those ways, not scaring people off.

**2. Hallucination**
- What it is: the model generates plausible-sounding but false information, with no internal signal that it's wrong.
- Why it happens (brief, non-technical): the model is optimized to produce fluent text, not to know what it doesn't know.
- Real-world example categories to include (swap in your own or well-documented public ones):
  - Fabricated citations/sources (e.g., lawyers sanctioned for citing nonexistent cases — this is well-documented publicly, worth a quick search for a current example)
  - Confidently wrong factual claims presented with no hedging
  - Invented statistics, quotes, or attributions
- How to catch it: ask for sources and check them independently; be suspicious of oddly specific numbers/quotes; cross-check anything you'll rely on for a decision.

**3. Overreliance / automation bias**
- What it is: trusting AI output more than warranted because it's fast, fluent, and confident-sounding.
- How it shows up at work: skipping the "would I have caught this myself" check; using AI output as a first draft that quietly becomes the final draft; deferring judgment on things outside the tool's competence.
- How to catch it: build in a deliberate review step; ask "what would I check if a junior colleague gave me this?"

**4. Accuracy degrades with stakes and specialization**
- General/low-stakes queries: usually fine.
- Specialized, current, or high-stakes queries (legal, medical, financial, safety-related): much higher failure risk.
- Rule of thumb: the more a wrong answer would cost you, the more independent verification it needs.

**5. Quick reference: red flags checklist**
- Overly specific claims with no source
- Requests outside the tool's likely training/knowledge
- Anything you're about to use without checking
- Anything where being wrong is costly or irreversible

**6. Transition line** into the next section: knowing the failure modes isn't a reason to avoid the tool — it's the basis for using it well.

---

### Section 2: Guidelines / Harm Reduction (covers "Practical Guidelines for Responsible Use Here" / "Good Judgment > Blanket Rules")

**1. Framing: why harm reduction, not prohibition**
- Blanket "never use it" rules tend to get ignored or pushed underground rather than followed — people use these tools regardless, often quietly.
- Goal here is good judgment and shared norms, not a rulebook that assumes bad faith.

**2. Principle-based guidelines** (rather than tool-by-tool rules)
- Verify before you rely: if you wouldn't stake your name on it, check it before it leaves your desk.
- Match scrutiny to stakes: light-touch for brainstorming/drafts, heavy-touch for anything client-facing, legal, financial, or safety-related.
- Disclose when it matters: be transparent with teammates/clients about AI-assisted work where it affects trust or accountability.
- Keep humans accountable: AI output is a draft or input, not a decision-maker — someone signs off.
- Protect sensitive data: don't paste confidential, client, or personal data into tools without knowing where it goes (link to your org's data policy here).

**3. What this looks like in practice**
- A short table or list of example use cases mapped to a comfort level (e.g., "brainstorming internal ideas" vs. "drafting external client communication" vs. "legal/compliance content") — leave placeholders for your team to fill in with real examples.

**4. What we're not saying**
- Not "AI is always fine" and not "AI is always bad" — the goal is calibrated judgment, matched to context and stakes.
- Acknowledge legitimate reasons people reach for these tools (time pressure, lack of in-house expertise, accessibility needs) rather than treating use as a personal failing.

**5. Where to go if unsure**
- Point to a person/channel for questions, and to your org's actual policy doc if one exists (link placeholder).

**6. Closing line** bridging to a "collective action" or "resources" section if your TOC has one next.

Want me to write full prose for either of these next, or keep going outline-first through the rest of the guide?