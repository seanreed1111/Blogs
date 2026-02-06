# Hello, World of Context Engineering

hello world blog I am a python programmer who builds multi-agent workflows. Spent time as data scientist and most recently as AI/ML engineer at a voice AI startup, and before that as forward deployed engineer for ML related topics. 

Use Plans, use GRAPHS, with Mermaid,  use guardrails, ask agent to check the work of a previous agent.

This will be an eclectic set of posts, driven by my interests. Plan to spend some time of multi agent frameworks like LangGraph.

The first N posts will definitely be about LangGraph. In particular, I will implement simple-ish projects with observability and workflow evaluations built in from the beginning.

Interleaved with posts about agentic workflows will be musings about agentic software development and context engineering, based on my own experiences starting with Cursor and now exclusively with Claude Code.

 my joirney of how to get production grade software using claude code skills, learning to implementing clean code and TDD and BDD, ML agents backed by feature stores, building an opentelemetry skill (and MCP server) and whatever else comes to mind.
 
My philosophy: building is best done in the open. I used to have a meetup called Python + Data Science, and this is how it started: (tell story) Blog a langraph agent with langfuse, retries, and timeouts Plan on doing the same thing here ◦ Hello, World of Context Engineering ◦ talk about my philosophy: 


## everyone is a software architect now. 
That includes all junior data scientists, data analysts, software engineers. if you are using AI coding tools, and you should be, then you must learn how to build software that lasts, understand what that looks like, and understand the tradeoffs that you are making when you don't follow best practices. Eyes wide open.

You are now the engineering manager of a team (or a fleet!) of tiny people living in your computer that can do amazing stuff, and they can also wreck everything you are working on. 

Star Trek TOS episode of the grown man with amazing power who was actually just a little boy looking to play.

story of one cent for the part and $10,000 for knowing which part was needed, and where the part should be placed. ◦ AI cannot answer those questions for you, because they don't have enough context as to what you are trying to accomplish. 

the question is: do you?? have you made a plan, checked it twice, found out if it is naughty or nice.? 

did you ask a NEW claude agent with a clear context to check the plan made by your PREVIOUS claude agent for errors and inconsistencies . Did you ask it if they plan could be run by a claude agent without ambiguity and without asking the user any questions? 

did you ask it with a clear context if it had any questions or doubts about the plan? you should ◦ I am also into multi agent workflows ◦ my pseudo toy example will be setting up a mcdonalds drive thru ordering bot with LangGraph

Me and my buddy claude (link to MyBuddy YT video) are gonna build things for you. mostly multi-agent workflows, some simple, some complicated. Some with Feature Stores pushing out batch and real-time predictions. 

But all will be done with observability, retries, evaluation metrics, deployments, etc. So, a mix of simple and not simple stuff. (see langchain academy) ◦ pydantic is important because any constraints you can put on llm output will only benefit you in the long run

why is learning data science like the beginning of The Divine Comedy?

Langfuse's first onboarding email says "Tracing is the foundation of reliable AI apps". I build apps with tracing as a first-class citizen, and you should, too. don't add tracing as an afterthought unless you're just hacking away a POC. But even then, you should put it in as early as possible. 

If you are trying to make agentic workflows  that are flexible and built to change as your requirements change? You MUST be the human in the loop. And you must have observability AND evals.

Design an agent workflow in claude to make plans for software. (Human in the Loop) ◦ how to do TDD with claude ◦ Blog a basic langgraph flow with langfuse observability and run in langfuse studio ◦ blog with langfuse prompt management ◦ blog with langfuse evals ◦ Hello, McDonald's Drive -Thru Agents - note that can use Send command to dispatch multiple orders and validate them ◦ Make an examples repo using returns python framework with a fastapi backend, then contribute it as open source ◦ there are only three items available: burger, fries, and shake. ◦ ◦ use dep injection ◦ ◦ for clientasync httpx for all requests. requests must have a valid auth token (123) in header. (assume received from previous flow) validate auth code when any request received. put auth code hash in the config. ◦ you can GET menu, POST an order of a single item, GET your current order, PUT an update to your current order including additions or deletions, or delete your entire order. if you try to order something not there, should get an error. your order can be empty, so that path should return a maybe. also, API calls can error out die to network or invalid/missing auth code(123) ◦ there should be an injectable local request time innthe header, for the later recommendation engines ◦ database should be thr sqlite rust database for python ◦ data model: item: itemid itemname, quantity ◦ combo: List[Item] ◦ order: orderid, Maybe(List[Item] | Combo) ◦ make llms.txt file for results framework. ◦ make MCP server for results framework ◦ serving predictions from feature stores: always recommend dessert if it is 5pm or later ◦ how do you dependency inject time, so it is always the time you want?????? ◦ Build feature store to serve batch/real time data for ML model endpoint ◦ if customer orderstwo or more items, suggest a dessert. or whatever your ML model recommends ◦ Multi-agent routing. add item, remove-item, ask questions. initial agent has to figure out which one the customer wants to do ◦ build langgraph MCP server ◦