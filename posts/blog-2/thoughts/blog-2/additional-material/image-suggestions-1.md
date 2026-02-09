# Image Suggestions for "Architecting the Agentic Harness"

A curated list of light-hearted, humorous images to break up the essay and add visual relief to what is otherwise a dense, technical piece. Each suggestion includes a link, placement recommendation, and reasoning.

---

## 1. XKCD #1838: "Machine Learning"

**Link:** [https://xkcd.com/1838/](https://xkcd.com/1838/)
**Direct image:** [https://imgs.xkcd.com/comics/machine_learning.png](https://imgs.xkcd.com/comics/machine_learning.png)
**License:** [CC BY-NC 2.5](https://creativecommons.org/licenses/by-nc/2.5/) (free to use with attribution)

**Where to insert:** After the opening section "The Model Is Not the Product" (after line 9, before the `---` divider).

**Reasoning:** This comic shows someone pouring data into a pile of linear algebra and stirring it until it "looks right." It perfectly captures the essay's central argument that people treat AI models as black-box magic, while the real engineering challenge is everything *around* the model. Placing it right after the essay's thesis ("the model is the engine, but the harness is the car") gives the reader a laugh that reinforces the point before diving into the technical meat.

---

## 2. XKCD #2173: "Trained a Neural Net"

**Link:** [https://xkcd.com/2173/](https://xkcd.com/2173/)
**Direct image:** [https://imgs.xkcd.com/comics/trained_a_neural_net.png](https://imgs.xkcd.com/comics/trained_a_neural_net.png)
**License:** CC BY-NC 2.5

**Where to insert:** After the "What Is an Agentic Harness?" section (after line 21, before the `---` divider).

**Reasoning:** The comic's punchline -- "I trained a neural net... to do it" (but the neural net is just a person) -- is a tongue-in-cheek foil to the essay's point that the hard part isn't the model's intelligence, it's making it work reliably. The section just finished explaining that a model "hallucinates, loses context, has no memory, and cannot coordinate with other systems." This comic provides a light moment that says: "yeah, sometimes a human is still the more reliable neural net."

---

## 3. "This Is Fine" Dog (KC Green)

**Link:** [https://programmerhumor.io/memes/this-is-fine](https://programmerhumor.io/memes/this-is-fine)
**Original source:** The comic is by KC Green from "Gunshow" webcomic. Widely available but check licensing for commercial use.

**Where to insert:** At the start of "Pillar 3: Reliability and Validation Frameworks" (after line 63, before the paragraph about 99.9%+ accuracy).

**Reasoning:** The reliability section opens with the line "The third pillar is the one that separates demos from production systems." The "This is Fine" dog -- sitting calmly in a burning room -- is the universally recognized symbol of a production system that is technically running but spiritually on fire. It's the perfect visual shorthand for what happens when you ship AI without validation loops, confidence scoring, and escalation paths. Every engineer who has ever pushed to prod on a Friday will feel this one.

---

## 4. XKCD #2347: "Dependency"

**Link:** [https://xkcd.com/2347/](https://xkcd.com/2347/)
**Direct image:** [https://imgs.xkcd.com/comics/dependency.png](https://imgs.xkcd.com/comics/dependency.png)
**License:** CC BY-NC 2.5

**Where to insert:** In the "Advanced Memory Systems: High-Fidelity RAG" section (after line 61, after the paragraph ending "one of the hardest engineering challenges in production AI").

**Reasoning:** This comic shows all of modern digital infrastructure as a towering stack of blocks, with the entire thing depending on one tiny piece maintained by "a random person in Nebraska." The RAG section makes the point that AI reasoning is only as good as its context -- and that context depends on fragile data pipelines, domain-specific chunking, and multi-stage retrieval. The Dependency comic visually captures how one weak link in that chain can bring the whole system down. It also lightens the mood at the end of the most technically dense section of the essay.

---

## 5. XKCD #1988: "Containers"

**Link:** [https://xkcd.com/1988/](https://xkcd.com/1988/)
**Direct image:** [https://imgs.xkcd.com/comics/containers.png](https://imgs.xkcd.com/comics/containers.png)
**License:** CC BY-NC 2.5

**Where to insert:** In the "Deep Architecture: Orchestration and Tooling" section (after line 43, after the paragraph about "microservices architecture applied to cognitive work").

**Reasoning:** The essay explicitly compares agentic orchestration to microservices and distributed systems. This XKCD comic shows someone solving the problem of making two programs work together by... just putting them on two separate computers and gluing them together. It's a playful jab at how containerization and microservices "solve" complexity by adding a different kind of complexity -- which is exactly the tension the essay describes when it talks about orchestrating probabilistic reasoning engines with traditional distributed systems patterns.

---

## 6. XKCD #2030: "Voting Software"

**Link:** [https://xkcd.com/2030/](https://xkcd.com/2030/)
**Direct image:** [https://imgs.xkcd.com/comics/voting_software.png](https://imgs.xkcd.com/comics/voting_software.png)
**License:** CC BY-NC 2.5

**Where to insert:** Near the end of the "Reliability and Validation Frameworks" section (after line 78, after the paragraph about SLOs, error budgets, and chaos engineering).

**Reasoning:** In the comic, an airplane engineer and an elevator engineer confidently vouch for their systems' safety, but a software engineer panics when asked about voting software. The essay has just finished arguing that reliability engineering for AI is borrowed from traditional SRE but applied to non-deterministic, semantically-failing systems. The comic captures the uncomfortable truth: software engineers *know* how fragile their systems are, and adding probabilistic AI into the mix only makes it worse. A well-timed laugh before the essay pivots to "What This Means for Modern Software Development."

---

## 7. "It Works on My Machine" Badge

**Link:** [https://programmerhumor.io/docker-memes/it-works-on-my-machine-kswk](https://programmerhumor.io/docker-memes/it-works-on-my-machine-kswk)
**Also available as stickers:** [https://www.teepublic.com/stickers/it-works-on-my-machine](https://www.teepublic.com/stickers/it-works-on-my-machine)

**Where to insert:** In the "The Competitive Moat Is the Harness, Not the Model" subsection (after line 108, after the paragraph about model-agnostic harnesses and swappable components).

**Reasoning:** The essay's argument here is that the model is a commodity -- everyone has access to the same GPT, Claude, Gemini. What matters is the harness. The "Works on My Machine" badge is a funny closer because it highlights the gap between "it works in my notebook/demo" and "it works in production at scale." The harness is literally the thing that bridges that gap. This image acts as a wink to the reader: "You know the demo worked. But can you ship it?"

---

## Summary: Suggested Placement Order

| # | Image | Insert After Section | Line Approx |
|---|-------|---------------------|-------------|
| 1 | XKCD #1838 (Machine Learning) | "The Model Is Not the Product" | ~Line 9 |
| 2 | XKCD #2173 (Trained a Neural Net) | "What Is an Agentic Harness?" | ~Line 21 |
| 3 | XKCD #1988 (Containers) | Orchestration pillar, after microservices comparison | ~Line 43 |
| 4 | XKCD #2347 (Dependency) | RAG pillar, end of section | ~Line 61 |
| 5 | "This Is Fine" Dog | Reliability pillar, opening | ~Line 63 |
| 6 | XKCD #2030 (Voting Software) | Reliability pillar, end of section | ~Line 78 |
| 7 | "Works on My Machine" Badge | Competitive moat subsection | ~Line 108 |

---

## Notes on Licensing

- **XKCD comics** (items 1, 2, 4, 5, 6) are licensed under [CC BY-NC 2.5](https://creativecommons.org/licenses/by-nc/2.5/). You can use them freely in a blog post as long as you attribute Randall Munroe / xkcd.com and the use is non-commercial.
- **"This Is Fine"** is by KC Green. It's widely shared but technically copyrighted. For a blog post, fair use likely applies if used for commentary/criticism, but consider linking rather than embedding if you want to be cautious.
- **"Works on My Machine"** is a community meme with no single author. The badge design is widely reproduced and available as stickers/merchandise from many sources.

## Sources Consulted

- [XKCD - Machine Learning](https://xkcd.com/1838/)
- [XKCD - Trained a Neural Net](https://xkcd.com/2173/)
- [XKCD - Dependency](https://xkcd.com/2347/)
- [XKCD - Containers](https://xkcd.com/1988/)
- [XKCD - Voting Software](https://xkcd.com/2030/)
- [Explain XKCD - AI Category](https://www.explainxkcd.com/wiki/index.php/Category:Artificial_Intelligence)
- [ProgrammerHumor.io - This is Fine](https://programmerhumor.io/memes/this-is-fine)
- [ProgrammerHumor.io - Microservices](https://programmerhumor.io/memes/microservices)
- [ProgrammerHumor.io - Deployment Memes](https://programmerhumor.io/memes/deployment)
- [CanIPhish - Top AI Memes 2026](https://caniphish.com/blog/ai-memes)
- [DataScienceDojo - Top AI Memes](https://datasciencedojo.com/blog/top-ai-memes-and-jokes/)
