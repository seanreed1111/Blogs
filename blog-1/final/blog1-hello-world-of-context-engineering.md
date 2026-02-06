# Hello, World of Context Engineering

I am a Python programmer who builds multi-agent workflows. I have spent time as a data scientist, as a forward-deployed engineer for machine learning projects, and most recently as an AI/ML engineer at a voice AI startup. Along the way I have become convinced of something: **building is best done in the open.**

Years ago I started a meetup called Python + Data Science. It began the way these things always do --- a handful of people in a room, talking through problems none of us had fully solved yet. The meetup grew because the work was visible. People could see what we were building, ask questions, poke holes, and contribute. The openness was the point.

This blog is the same idea, applied to a different moment in software. The field has shifted underneath all of us, and I want to work through that shift out loud.

---

## Everyone Is a Software Architect Now

If you are using AI coding tools --- and you should be --- then you are a software architect whether you signed up for the title or not.

This is true for junior data scientists, data analysts, and software engineers alike. The moment you hand a task to an AI agent, you have made an architectural decision. You have decided what to delegate, what constraints to impose, and what to trust without verifying. If you do not understand the tradeoffs you are making when you skip best practices, you will pay for it later. Eyes wide open.

Here is how I think about it. You are now the engineering manager of a fleet of tiny people living inside your computer. They can do astonishingly complex tasks. They can also wreck your life and the lives of your coworkers and your entire production system. If you have ever seen *The Squire of Gothos* --- the Star Trek TOS episode where Trelane has godlike power but turns out to be a child just looking to play --- that is the dynamic. Immense capability, no judgment. The judgment has to come from you.

You have probably heard the old tale about the engineer who charged $10,000 to fix a machine. One dollar for turning the right screw, $9,999 for knowing which screw to turn.

We are all that engineer now. The coding --- the screw-turning --- is increasingly handled by AI. Your deep value is knowing *which* screw to turn. And that knowledge is not generic. It is knowledge about your specific system, your company's software stack, your customer requirements, your SLAs, your regulatory constraints. AI cannot answer those questions for you, because it does not have enough context about what you are trying to accomplish.

Which raises the real question.

---

## Context Engineering: The Core Idea

Do *you* know what you are trying to accomplish?

Have you made a plan? Have you checked it? Have you pressure-tested it against the things that could go wrong?

This is what I mean by context engineering. It is the discipline of ensuring that every AI agent you work with has exactly the right information, constraints, and structure to do its job well. It is not about writing better prompts. It is about building better *contexts* --- the plans, the graphs, the guardrails, the validation loops that turn a probabilistic language model into a reliable collaborator.

Here is what that looks like in practice. You make a plan. You diagram it --- I use Mermaid graphs, because they are readable by both humans and agents. You set guardrails around what the agent can and cannot do. And then, critically, you ask a *new* agent with a clean context to review the plan your *previous* agent produced.

Did the reviewer find errors or inconsistencies? Could the plan be executed by an agent without ambiguity, without needing to stop and ask the user clarifying questions? Does the reviewer have any doubts?

If the answer to that last question is yes, you are not done planning.

The human must remain in the loop. If you are trying to build agentic workflows that are flexible and built to change as your requirements change, you must be the one steering. And you must have observability and evaluations in place so you can actually see what is happening. Otherwise you are flying blind with a co-pilot who is confident but not always correct.

---

## The Agentic Harness: A Preview

This brings me to a bigger idea that I will explore fully in my next post, *Architecting the Agentic Harness: The Real Engineering Behind AI That Actually Works*.

The short version: **the model is the engine, but the harness is the car.**

The conversation around AI is still dominated by model benchmarks, parameter counts, and reasoning scores. But the builders who are shipping production AI systems have already moved on. They understand that the hard problem is no longer making models smarter. The hard problem is making them *reliable, coordinated, and useful* inside real systems that serve real users.

This is not prompt engineering. This is systems engineering applied to a new class of compute primitive.

The agentic harness --- the production-grade software that sits between foundation models and the messy real world --- rests on three pillars:

1. **Deep Architecture.** Orchestration and multi-agent coordination. This is microservices patterns applied to cognitive work: service decomposition, message passing, state management, retry logic, circuit breakers --- except your compute primitives are probabilistic reasoning engines instead of deterministic functions.

2. **Advanced Memory Systems.** High-fidelity retrieval-augmented generation. Not the demo version that chunks documents into fixed-size blocks and calls it a day, but the production version: domain-specific chunking, multi-stage retrieval, and context assembly that gives the reasoning model exactly the right information at the right time.

3. **Reliability and Validation.** Reasoning loops where a reviewer agent critiques a drafter agent's work. Confidence scoring that is empirically calibrated. Escalation paths to humans when the system cannot resolve disagreements. Audit trails that capture every step of the reasoning process.

Every company has access to the same foundation models. The competitive moat is not the model. It is the harness. The next post will go deep on all three pillars.

---

## What This Blog Will Cover

This will be an eclectic set of posts, driven by my interests. They will be organized around three threads that weave in and out of each other.

### Multi-Agent Workflows with LangGraph

The first series of posts will focus on LangGraph. I will build real projects with observability and workflow evaluations baked in from the very beginning --- not bolted on as an afterthought.

The first project: **Hello, McDonald's Drive-Thru Agents.** A multi-agent ordering bot built with LangGraph. Three items on the menu --- burger, fries, and shake --- and a set of specialized agents that route customer requests: one to add items, one to remove items, one to answer questions. Simple on the surface, but layered with the things that matter in production: observability and tracing via Langfuse, prompt management through Langfuse, workflow evaluations with Langfuse evals, feature store integrations, a recommendation engine, and dependency injection patterns that keep the whole thing testable.

It is a toy domain with production-grade engineering. That is the point.

### Observability and Evaluation as First-Class Citizens

Langfuse's first onboarding email says: *"Tracing is the foundation of reliable AI apps."* I agree. I build applications with tracing as a first-class citizen, and you should too.

Do not add tracing as an afterthought. Do not tell yourself you will get to it later. Even if you are just hacking away at a proof of concept, put observability in as early as possible. You will thank yourself when something breaks at 2 AM and you can actually see what happened.

This thread will cover Langfuse tracing, prompt management, evals, and studio. It will also cover the production patterns that keep agentic workflows running: retries, timeouts, and graceful degradation.

### Agentic Software Development and Context Engineering

Interleaved with the build posts will be essays and musings about agentic software development itself --- the meta-game of building production-grade software with AI coding tools.

I started with Cursor and now work exclusively with Claude Code. This thread will cover what I have learned along the way: how to do TDD and BDD with an AI collaborator, why Pydantic is essential for constraining LLM output, how to build an OpenTelemetry skill and an MCP server, and the broader journey of figuring out how to get production-grade software out of a human-AI partnership.

---

## How We Will Build

Me and my buddy Claude are going to build things for you. Mostly multi-agent workflows --- some simple, some complicated. Some backed by feature stores pushing out batch and real-time predictions. But all of them will be built with the same core principles:

**Observability from the start.** Every project ships with tracing, not as a nice-to-have, but as a requirement.

**Evaluations from the start.** If you cannot measure whether your agents are doing the right thing, you do not have a production system. You have a demo.

**Retries, timeouts, and error handling.** Because production systems fail, and the question is not whether they will fail but how gracefully they recover.

**Open-source where possible.** I plan to contribute examples and tooling back to the community. Building in the open means the artifacts are open too.

This will be a mix of accessible entry points and real-world depth. Some posts will be straightforward walkthroughs. Others will get into the weeds. All of them will treat the engineering seriously.

---

## What's Next

That is the invitation. Come build in the open with me.

Up next: *Architecting the Agentic Harness* --- a deep dive into the three pillars of production AI systems and why the harness, not the model, is where the real engineering happens.

Then: the first build. Hello, McDonald's Drive-Thru Agents --- a multi-agent ordering bot with LangGraph and Langfuse, built from scratch with observability, prompt management, and evals from the very first line of code.

Let's get to work.
