---
layout: page
title: "Notes from Holes in the web on Aeon"
notes: true
added: 2025-10-20
updated: 2025-10-23
---

[Generative AI has access to a small slice of human knowledge - Aeon Essays](https://aeon.co/essays/generative-ai-has-access-to-a-small-slice-of-human-knowledge)

- **Lots of human knowledge is missing from the internet, which means AI is missing lots of human knowledge**
    - oral cultures
    - many languages are under-represented or absent
- **The world has profound power imbalances and these are reflected in the digital world. AI amplifies and may entrench these imbalances.**
- Many people are using AI as their primary way to learn about the world
    - Search engines are putting AI answers first
- **Over time, Western approaches to knowledge and knowing have come to be seen as objective and universal, rather than culturally situated or historically contingent**
- By design, in LLMs ideas that appear more often and more widely are more strongly encoded
    - This creates a feedback loop that narrows information and knowledge
    - In particular: "mode amplification". The mode average is the value that appears most often in a set.
- **Uneven internal knowledge representation and mode amplification in output generation help explain why LLMs often reinforce dominant cultural patterns or ideas**
- The uneven encoding gets further skewed through reinforcement learning from human feedback (RLHF)
- **"Knowledge collapse"**: narrowing of available information, declining awareness of alternatives, due to less frequent retrival or citation

## Gathered notes

- Huge swathes of human knowledge are missing from the internet. By definition, generative AI is shockingly ignorant too
- the digital world reflects profound power imbalances in knowledge, and how this is amplified by generative AI with the rise of GenAI  that asymmetry threatens to become entrenched.
- For many people, GenAI is becoming their primary way to learn about the world.
- The most popular models privilege dominant epistemologies (typically Western and institutional) while marginalising alternative ways of knowing, especially those encoded in oral traditions, embodied practice and the languages considered ‘low-resource’
- this training data is far from the sum total of human knowledge. As well as oral cultures, many languages are underrepresented or absent.
- When AI systems lack adequate exposure to a language, they have blind spots in their comprehension of human experience.
- English is spoken by approximately 20 per cent of the global population (including both native and non-native speakers), but it dominates the digital space by an exponentially larger margin.
- In the computing world, approximately 97 per cent of the world’s languages are classified as ‘low-resource’. ... ‘high-resource’ languages have abundant and diverse digital data available.
- the idea of cultural hegemony developed by the Italian philosopher Antonio Gramsci.
-  Over time, epistemological approaches rooted in Western traditions have come to be seen as objective and universal, rather than culturally situated or historically contingent. 
- By design, LLMs also tend to reproduce and reinforce the most statistically prevalent ideas, creating a feedback loop that narrows the scope of accessible human knowledge.
- The internal representation of knowledge in an LLM is not uniform. Concepts that appear more frequently, more prominently, or across a wider range of contexts in the training data tend to be more strongly encoded. Not because the LLM likes pizza, but because that association is more statistically prominent.
- More subtly, the model’s output distribution does not directly reflect the frequency of ideas in the training data. Instead, LLMs often amplify dominant patterns in a way that distorts their original proportions. This phenomenon can be referred to as ‘mode amplification’.
- Together, these two principles – uneven internal knowledge representation and mode amplification in output generation – help explain why LLMs often reinforce dominant cultural patterns or ideas.
- This uneven encoding gets further skewed through reinforcement learning from human feedback (RLHF), where GenAI models are fine-tuned based on human preferences. This inevitably embeds the values and worldviews of their creators into the models themselves.
- And beyond merely reflecting existing knowledge hierarchies, GenAI has the capacity to amplify them, as human behaviour changes alongside it.
- ‘knowledge collapse’, a gradual narrowing of the information humans can access, along with a declining awareness of alternative or obscure viewpoints. not because it lacks merit, but because it is less frequently retrieved or cited.
- Peterson also warns of the ‘streetlight effect’, named after the joke where a person searches for lost keys under a streetlight at night because that’s where the light is brightest. In the context of AI, this would be people searching where it’s easiest rather than where it’s most meaningful. Over time, this would result in a degenerative narrowing of the public knowledge base, driven not by censorship but convenience and algorithms.
- The rationale isn’t that research-backed advice is always right or risk-free. It’s that it offers a defensible position if something goes wrong.
- It’s a compromise shaped by the structural context, not based on what’s most useful or true.
- The marginalisation of local and Indigenous knowledge has long been driven by entrenched power structures. GenAI simply puts this process on steroids.

## Raw notes

- **Huge swathes of human knowledge are missing from the internet. By definition, generative AI is shockingly ignorant too**
- responsible AI systems. My work has been revealing to me how **the digital world reflects profound power imbalances in knowledge, and how this is amplified by generative AI** (GenAI). The early internet was dominated by the English language and Western institutions, and this imbalance has hardened over time, leaving whole worlds of human knowledge and experience undigitised. Now **with the rise of GenAI** – which is trained on this available digital corpus – **that asymmetry threatens to become entrenched**.
- **For many people, GenAI is becoming their primary way to learn about the world.**
- These systems may appear neutral, but they are far from it. Th**e most popular models privilege dominant epistemologies (typically Western and institutional) while marginalising alternative ways of knowing, especially those encoded in oral traditions, embodied practice and the languages considered ‘low-resource’** in the computing world, such as Hindi or Swahili, both spoken by hundreds of millions.
- What’s at stake then isn’t just representation – it’s the resilience and diversity of knowledge itself.
- **this training data is far from the sum total of human knowledge. As well as oral cultures, many languages are underrepresented or absent.**
- Each language carries entire worlds of human experience and insight developed over centuries: the rituals and customs that shape communities, distinctive ways of seeing beauty and creating art, deep familiarity with specific landscapes and natural systems, spiritual and philosophical worldviews, subtle vocabularies for inner experiences, specialised expertise in various fields, frameworks for organising society and justice, collective memories and historical narratives, healing traditions, and intricate social bonds.
- **When AI systems lack adequate exposure to a language, they have blind spots in their comprehension of human experience.**
- the imbalance between how many people speak a language in the physical world and how much that language is represented in online data.
- **English is spoken by approximately 20 per cent of the global population (including both native and non-native speakers), but it dominates the digital space by an exponentially larger margin.**
- **In the computing world, approximately 97 per cent of the world’s languages are classified as ‘low-resource’. ... ‘high-resource’ languages have abundant and diverse digital data available.**
- To illustrate the kinds of knowledge missing, let’s consider just one example: our understanding of local ecologies.
- To understand how certain ways of knowing rise to global dominance, often at the expense of Indigenous knowledge, it helps to consider **the idea of cultural hegemony developed by the Italian philosopher Antonio Gramsci.**
- Gramsci argued that power is not maintained solely through force or economic control, but also through the shaping of cultural norms and everyday beliefs. **Over time, epistemological approaches rooted in Western traditions have come to be seen as objective and universal, rather than culturally situated or historically contingent.** This has normalised Western knowledge as the standard, obscuring the specific historical and political forces that enabled its rise. Institutions such as schools, scientific bodies and international development organisations have helped entrench this dominance.
- Epistemologies are not just abstract and cognitive. They are physically embodied around us, with a direct impact on our bodies and lived experiences. To understand why, let’s consider an example that contrasts sharply with the kind of Indigenous construction practices that Dharan seeks to revive: high-rise buildings with glass façades in the tropics.
- In her book Decolonising Methodologies (1999), the Māori scholar Linda Tuhiwai Smith emphasises that colonialism profoundly disrupted local knowledge systems – and the cultural and intellectual foundations upon which they were built – by severing ties to land, language, history and social structures. Smith’s insights reveal how these processes are not confined to a single region but form part of a broader legacy that continues to shape how knowledge is produced and valued. It is on this distorted foundation that today’s digital and GenAI systems are built.
- **By design, LLMs also tend to reproduce and reinforce the most statistically prevalent ideas, creating a feedback loop that narrows the scope of accessible human knowledge.**
- Why so? **The internal representation of knowledge in an LLM is not uniform. Concepts that appear more frequently, more prominently, or across a wider range of contexts in the training data tend to be more strongly encoded.** For example, if pizza is commonly mentioned as a favourite food across a broad set of training texts, the model is more likely to respond with ‘pizza’ when asked ‘What’s your favourite food?’ **Not because the LLM likes pizza, but because that association is more statistically prominent.**
- A few years back, my dad was diagnosed with a tumour on his tongue – which meant we had some choices to weigh up. My family has an interesting dynamic when it comes to medical decisions. While my older sister is a trained doctor in Western allopathic medicine, my parents are big believers in traditional remedies. Having grown up in a small town in India, I am accustomed to rituals. My dad had a ritual too. Every time we visited his home village in southern Tamil Nadu, he’d get a bottle of thick, pungent, herb-infused oil from a vaithiyar, a traditional doctor practising Siddha medicine. It was his way of maintaining his connection with the kind of medicine he had always known and trusted.
- Dad’s tumour showed signs of being malignant, so the hospital doctors and my sister strongly recommended surgery. My parents were against the idea, worried it could affect my dad’s speech. This is usually where I come in, as the expert mediator in the family. Like any good millennial, I turned to the internet for help in guiding the decision. After days of thorough research, I (as usual) sided with my sister and pushed for the surgery. The internet backed us up.
- We eventually got my dad to agree and even set a date. But then, he slyly used my sister’s pregnancy as a distraction to skip the surgery altogether. While we pestered him every day to get it done, he was secretly taking his herbal concoction. And, lo and behold, after several months the tumour actually shrank and eventually disappeared. That whole episode definitely earned my dad some bragging rights.
- At the time, I dismissed it as a lucky exception. But recently I’ve been wondering if I was too quick to dismiss my parents’ trust in traditional knowledge, while easily accepting the authority of digitally dominant sources. I find it hard to believe my dad’s herbal concoctions worked, but I have also since come to realise that the seemingly all-knowing internet I so readily trusted contains huge gaps – and in a world of AI, it’s about to get worse.
- **More subtly, the model’s output distribution does not directly reflect the frequency of ideas in the training data. Instead, LLMs often amplify dominant patterns in a way that distorts their original proportions. This phenomenon can be referred to as ‘mode amplification’.**
- **Together, these two principles – uneven internal knowledge representation and mode amplification in output generation – help explain why LLMs often reinforce dominant cultural patterns or ideas.**
- **This uneven encoding gets further skewed through reinforcement learning from human feedback (RLHF), where GenAI models are fine-tuned based on human preferences. This inevitably embeds the values and worldviews of their creators into the models themselves.**
- Commercial pressures add another layer entirely.
- **And beyond merely reflecting existing knowledge hierarchies, GenAI has the capacity to amplify them, as human behaviour changes alongside it.**
- The integration of AI overviews in search engines, along with the growing popularity of AI-powered search engines such as Perplexity, underscores this shift. ... Previously, people had to browse multiple links to compare viewpoints and gather comprehensive information. Now, they can read AI-generated summaries.
- The internet, as the primary source of knowledge for AI models, becomes recursively influenced by the very outputs those models generate. With each training cycle, new models increasingly rely on AI-generated content, reinforcing prevailing narratives and further marginalising less prominent perspectives. This risks creating a feedback loop where dominant ideas are continuously amplified while long-tail or niche knowledge fades from view.
- The AI researcher Andrew Peterson describes this phenomenon as **‘knowledge collapse’, a gradual narrowing of the information humans can access, along with a declining awareness of alternative or obscure viewpoints.** As LLMs are trained on data shaped by previous AI outputs, underrepresented knowledge can become less visible – **not because it lacks merit, but because it is less frequently retrieved or cited.**
- **Peterson also warns of the ‘streetlight effect’, named after the joke where a person searches for lost keys under a streetlight at night because that’s where the light is brightest. In the context of AI, this would be people searching where it’s easiest rather than where it’s most meaningful. Over time, this would result in a degenerative narrowing of the public knowledge base, driven not by censorship but convenience and algorithms.**
- AI developers might argue that this is simply a data problem, solvable by incorporating more diverse sources into training datasets. While that might be technically possible, the challenges of data sourcing, prioritisation and representation are far more complex than such a solution implies.
- **The rationale isn’t that research-backed advice is always right or risk-free. It’s that it offers a defensible position if something goes wrong.**
- **It’s a compromise shaped by the structural context, not based on what’s most useful or true.**
- **The marginalisation of local and Indigenous knowledge has long been driven by entrenched power structures. GenAI simply puts this process on steroids.**
- Wohlleben’s broader point is that the health of a system depends on the presence of all its parts, even those that might seem inconsequential.

