---
layout: page
title: AI Literacy
ai: true
added: 2026-07-21
updated: 2026-07-21
---


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