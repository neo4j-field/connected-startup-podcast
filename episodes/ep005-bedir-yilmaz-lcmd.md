# Episode 005 — Bedir Yilmaz, lcmd

**Air date:** October 15, 2026  
**Guest:** Dr. Bedir Yilmaz, AI Architect, lcmd

---

## Watch & Listen

- **YouTube:** [Watch on YouTube](https://www.youtube.com/watch?v=ykjoIgDPm3s)
- **LinkedIn:** [Watch on LinkedIn](https://www.linkedin.com/events/7515822170078433280/)

---

## About Bedir Yilmaz

Dr. Bedir Yilmaz is AI Architect at lcmd. He comes from a computer vision research background — a PhD on crowd counting and density estimation, including three years of research in Malaysia — and had no prior construction industry experience before joining lcmd about six months ago (April 2026) to build out the company's AI capabilities from scratch.

---

## About lcmd

lcmd is a Stuttgart-based lean construction management platform spun out of Drees & Sommer. It's used on complex, multi-year construction projects, including Germany's largest particle accelerator for antiproton research and the rail tunnel connecting Denmark and Germany. lcmd is an official member of the Neo4j Startup Program.

- **Website:** [lcmd.io](https://lcmd.io/)

## Episode Summary

Dr. Bedir Yilmaz, a computer-vision PhD turned AI Architect at lcmd, explains how the company's first attempt at a construction-site conversational agent — a RAG pipeline built over AI-generated prose narratives of project activity — could answer "what already happened" questions but failed at the sense-making questions site experts actually needed, like what's threatening a project's timeline. That gap pushed him toward a Neo4j knowledge graph, built using agentic construction techniques, which now spans 108 projects with roughly 25 million nodes and 83 million relationships in private beta. The graph powers "Consultant in a Box," a natural-language agent that generates Cypher on the fly and surfaces fleet-wide construction wisdom — like which trade typically precedes drywall — without exposing any single customer's private project data.

---

## Topics Covered

- lcmd: a Stuttgart-based lean construction management platform spun out of Drees & Sommer, used on complex multi-year builds like Germany's largest particle accelerator for antiproton research and the Denmark–Germany rail tunnel
- From computer vision PhD to construction AI: Bedir's path from crowd counting/density estimation research into an AI Architect role with no prior construction background
- The original goal: a conversational engine letting construction site teams talk to their own project data
- Why the app's collaborative, highly efficient source data wasn't usable by LLMs in its raw form, and the first fix: using coding agents to transform it into prose narrative corpora for a traditional RAG pipeline
- Where RAG hit its ceiling: it could answer "what already happened" questions (who's the most influential person, what happened last month) but site experts needed sense-making questions about the past and future — like what's threatening the project timeline — that similarity search can't answer because it ranks by linguistic closeness, not construction-domain logic
- The graph moment: realizing the missing connections were logical, not linguistic, and that a knowledge graph — not GraphRAG, which got too costly at lcmd's scale — was the way to represent that construction logic
- Building the graph with agentic construction, inspired by Andreas Kollegger's Coursera lectures on agentic knowledge graph construction, and reaching near-parity with lcmd's own API within about an hour of applying what he'd learned
- Current scale: 108 projects loaded into one connected graph (~25M nodes, ~83M relationships) — in private beta, not yet GA
- Why a shared, multi-tenant graph works: project schemas are structurally similar (trades, tasks, dependencies), letting lcmd answer cross-project "wisdom of construction" questions without surfacing any customer's private data
- "Consultant in a Box" — lcmd's natural-language agent, built on a custom text-to-Cypher engine plus pre-built query templates for anticipated questions, with text-to-Cypher reserved for the ones it can't anticipate
- Why entity resolution hasn't been a problem: the knowledge graph is built deterministically from lcmd's own structured application data (trade selection, task dependencies, start/end dates), not extracted from unstructured text
- lcmd's product thesis: the knowledge graph is the product, not just a means — the long-term vision is letting other people's agents query lcmd's construction knowledge at a fair market price
- lcmd is now an official member of the Neo4j Startup Program and is already putting its Aura credits to use

## Links Mentioned

- **lcmd:** [lcmd.io](https://lcmd.io/)
- **Neo4j Startup Program:** [neo4j.com/startup-program](https://neo4j.com/startup-program/)
- **Andreas Kollegger's Coursera lectures on agentic construction of knowledge graphs** (referenced repeatedly as the source of lcmd's approach): [coursera.org/projects/knowledge-graphs-rag](https://www.coursera.org/projects/knowledge-graphs-rag)
- **Text2Cypher** — the Neo4j library discussed as an alternative to lcmd's custom text-to-Cypher engine: [github.com/neo4j-labs/text2cypher](https://github.com/neo4j-labs/text2cypher)
- **Neo4j NODES** — Neo4j's annual virtual conference, mentioned as taking place November 12: [neo4j.com/nodes](https://neo4j.com/nodes/)
