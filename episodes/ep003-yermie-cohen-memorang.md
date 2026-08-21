# Episode 003 — Dr. Yermie Cohen, Memorang

**Air date:** August 20, 2026  
**Guest:** Dr. Yermie Cohen, Founder & CEO, Memorang

---

## Watch & Listen

- **YouTube:** [Watch on YouTube](https://www.youtube.com/watch?v=CysUrZzE7JM)
- **LinkedIn:** [Watch on LinkedIn](https://www.linkedin.com/events/7493680478932123648/)

---

## About Dr. Yermie Cohen

Dr. Yermie Cohen, MD, is the Founder and CEO of Memorang. Over 15 years in education technology, he has developed the curriculum and technology behind hundreds of test-prep programs reaching millions of learners across healthcare, professional licensure, and English proficiency. He pioneered machine-learning-powered spaced repetition in the early 2010s and launched one of the first applications of LLM-generated educational content in early 2022. Today, he builds multi-agent systems and Knowledge Graphs for high-stakes assessment and adaptive learning. He holds multiple engineering degrees from MIT and a Doctor of Medicine from UCLA.

---

## About Memorang

Memorang is building **the AI stack for education**, a vertically integrated platform for adaptive learning and assessment. After [winning the inaugural Vercel AI Accelerator](https://x.com/vercel/status/1694465309749473287) from a field of thousands of companies, Memorang built an enterprise platform that powers high-stakes assessments and personalized learning experiences at scale. Its Neo4j-powered Knowledge Graph transforms fragmented curricula, content, assessments, and learner data into structured, queryable institutional memory. AI agents use that foundation to automate curriculum development, content generation, psychometric evaluation, and personalization, while web and mobile apps bring those capabilities to market. Memorang is backed by [ETS Capital](https://www.ets.org/newsroom/ets-capital-expands-portfolio-with-investment-in-memorang.html).

- **Website:** [memorang.com](https://memorang.com/)

## Episode Summary

Yermie has been thinking in graphs since medical school — he'd sketched a graph model for pharmacology and anatomy before graph databases existed as a cloud service. When he set out to build Memorang's AI stack for education, he started with Neptune and moved to Neo4j for Cypher's standardization, deeper traversal performance, and managed hosting. The result: learner-data retrieval that took 8–9 seconds in Postgres now runs in under 500 milliseconds.

The deeper insight is how Memorang uses the graph not just to store curriculum and learner data, but to control every AI agent in the system. Rather than relying on semantic matching to route tools, sub-agents, and evaluators — which Yermie puts at around 70–80% accuracy — Memorang encodes subgraph membership in each skill's metadata so the right procedural memory and the right evaluator are called deterministically. For high-stakes assessment, where agent output has to be legally defensible in court, that precision isn't optional.

---

## Topics Covered

- Building Memorang's knowledge graph from a systems-engineering mindset — why relational databases break at depth two or three in curriculum modeling
- From Neptune to Neo4j: Gremlin's lack of standardization, missing managed hosting, and the hiring challenges that drove the switch
- The knowledge graph ontology: thick branches (subject areas), topical nodes, artifacts (items), and user-interaction edges
- Item response theory via nearest-neighbor graph traversal: predicting mastery on content a learner has never seen
- Infinite content generation + graph-weighted curriculum = ROI-based study scheduling
- Graph-controlled agent routing: encoding subgraph membership in skill YAML front matter to replace semantic tool calling with deterministic dispatch
- Reducing learner-data retrieval from 8–9 seconds to ~500 ms using Neo4j traversal optimization, caching, and query parallelization
- Hybrid architecture: Supabase (Postgres) + Neo4j + Redis, kept in sync via database triggers, each doing what it does best
- Applying conditionally selected evaluators to agent traces for high-stakes, legally defensible assessment content
- Hill climbing from 50% to 90% agent-output alignment with fewer than 100 human annotations by optimizing narrow, graph-scoped context rather than monolithic system prompts
- Roadmap: high-profile enterprise launches through end of 2026, general-availability developer platform in early 2027
