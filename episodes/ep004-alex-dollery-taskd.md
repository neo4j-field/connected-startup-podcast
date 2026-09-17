# Episode 004 — Alex Dollery, Taskd

**Air date:** September 17, 2026  
**Guest:** Alex Dollery, Co-founder & CTO, Taskd

---

## Watch & Listen

- **YouTube:** [Watch on YouTube](https://www.youtube.com/watch?v=MOT3LvWMRug)
- **LinkedIn:** [Watch on LinkedIn](https://www.linkedin.com/events/7505328681788227585/)

---

## About Alex Dollery

Alex Dollery is co-founder and Chief Technology Officer of Taskd, which is building connected company knowledge that brings facts, relationships, rules and evidence together for people and AI agents. His focus is making that knowledge a lasting business asset that remains useful as models, tools and workflows change.

He first encountered Neo4j around twelve years ago at BenevolentAI, working on a biomedical knowledge graph for drug discovery. He later served as a director of AI and Machine Learning at the London Stock Exchange Group.

---

## About Taskd

Taskd connects business information, expert rules and operational history so AI workflows can act reliably, explain their work and keep people in control of consequential decisions.

- **Website:** [taskd.ai](https://taskd.ai/)

## Episode Summary

Alex Dollery, co-founder and CTO of Taskd, explains why relational databases break down once you're storing many different shapes of data and need AI to reason over how it all connects — and how Taskd wraps logical rules and "concept graphs" around raw facts in Neo4j to produce explainable, evidence-backed answers. He walks through a real government hackathon build that turned 14 siloed databases into a rules-driven graph to flag suspicious multi-company transactions, then demos Sage, Taskd's upcoming natural-language query engine that answers questions from a document graph without leaning on a large LLM. Taskd is now working with paying customers — including a maritime industry client at 97.3% accuracy — and is looking to talk to teams that need to trace AI-driven decisions back to verifiable source data.

---

## Topics Covered

- What Taskd does: merging a graph database with logic to provide an evidence trail behind facts, answers, and decisions
- Why relational databases (Postgres) break down once data gets more varied in shape, and why a graph gives the flexibility to model it
- Moving beyond ontology into "concept graphs" — layered concepts and the relationships between them, not just raw data
- Why graph traversal makes it possible to infer connections across nodes that would require painful joins in a relational database
- Live demo: the Alberta government hackathon — 14 siloed databases turned into a graph (~9M nodes, ~38M with derived concepts), layered with rules to flag suspicious inter-company transactions and multi-board-member ownership patterns
- Agents that continuously enhance and expand the concept graph over time
- Bitemporal modeling — reasoning about what was known "as of" a past point in time vs. what's known now, and why that matters for financial/quant use cases
- Live demo: Sage, Taskd's upcoming query engine — answering natural-language questions from a news article corpus by traversing the concept graph, without a large LLM, and tracing every answer back to source evidence
- The neurosymbolic approach: small fine-tuned language models paired with a structured graph, rather than large frontier LLMs or GraphRAG, for reliable and cost-efficient reasoning
- Support from Mila (the Quebec AI research institute) and the city of Montreal
- Where Taskd is now: paying customers (97.3% accuracy with a maritime industry client), actively growing, and looking to talk to teams that need explainable, source-traceable AI decisions without heavy LLM costs

## Links Mentioned

- **Taskd:** [taskd.ai](https://taskd.ai/)
- **Alberta government hackathon case study** (demoed on air): [taskd-governance.pages.dev](https://taskd-governance.pages.dev/?src=taskd-site)
- **Mila** — Quebec AI research institute (mentioned as a supporter): [mila.quebec](https://mila.quebec/)
- **Neo4j Startup Program:** [neo4j.com/startup-program](https://neo4j.com/startup-program/)
