# Episode 006 — Ric Vezza, VH3 AI

**Air date:** November 19, 2026  
**Guest:** Ric Vezza, Founder & CTO, VH3 AI

---

## Watch & Listen

- **YouTube:** [Watch on YouTube](https://www.youtube.com/watch?v=QAdbm7V0uzE)
- **LinkedIn:** [Watch on LinkedIn](https://www.linkedin.com/events/7528490182103449600/)

---

## About Ric Vezza

Ric Vezza is the founder and CTO of VH3 AI, the AI operating layer for field service. He spent 15 years in enterprise security systems — the first seven as a field service engineer, and the next seven in senior leadership, heading up sales and growing the business significantly. At the end of 2017 he founded VH3, which for nine years has put technology into field service businesses. In 2022 the team started building machine learning applications, and that work became VH3 AI in 2024.

---

## About VH3 AI

VH3 AI is the AI operating layer for field service, helping businesses adopt AI across the whole organisation, from the back office to the engineers in the field. The API-first solution combines a Neo4j knowledge graph with semantic indexing, so every job is connected to its customer, site, engineer and history, and can be found by meaning, not just keywords. AI agents for operations, technical and sales then put that knowledge to work — planning the day, sorting the inbox, processing worksheets and photos, and answering anyone's question in plain English.

VH3 has analysed more than 450,000 jobs for businesses with over 1,000 engineers and a combined turnover of over £350 million, and won Best AI Startup of the Year 2026 at the UK Business Tech Awards.

- **Website:** [vh3.ai](https://www.vh3.ai)

## Episode Summary

Ric Vezza, founder and CTO of VH3 AI, explains how his team's first field service agents, which called SaaS platform APIs at run time, couldn't carry context across the customers, sites, parent accounts, engineers and jobs that make up a field service business. That pushed them to ingest and normalise each client's data into a Neo4j knowledge graph, paired with a separate, deliberately granular semantic index. The graph now resolves over 90% of inbound job requests from about 20 sources on the first pass, with a human choosing from pre-built options when confidence is low, and it powers about 20 "sentinel" monitors that are almost pure graph reads. Ric also covers keeping a graph trustworthy over time through provenance, why VH3 aims to enable customers rather than lock them in, and why they should own their data.

---

## Topics Covered

- What field service is: any business sending engineers out to fix problems, from cleaning to security systems. Work is largely reactive and often emergency or critical, and the challenges are access to information, turning up with the right parts, and getting from call to cash quickly
- VH3's path: eight or nine years of integration work for field service businesses, then generative AI arriving at the end of 2022 with strong early use cases around unstructured data, such as engineer briefing calls on the way to visits
- Where run-time API calls fell short: SaaS platform APIs return disjointed entities (customers, sites, parent-child hierarchies, engineers, vehicles, assets, jobs, worksheets) that have to be stitched together call by call, and early search tolerated almost no misspelling
- The case for owning your data: the work that matters to a business should stay inside it, which led VH3 to start ingesting client data rather than fetching it
- Why not RAG alone or SQL: RAG has its limits, and plumbing up joins across tables to make them dynamic proved "a bit of a fool's errand"
- Job types and processes evolve over the years (a boiler service might have had a different job type and worksheet in 2022), leaving disparate records for the same thing. Defining what a job, record or customer is in the graph ontology normalises across clients and across multiple field service management systems, including portfolio companies that acquire businesses on different platforms
- The graph moment: edges as a dynamic layer, with "maybe", "could be" and "was" relationships that can change quickly, and Cypher letting an agent traverse three hops across hundreds of relevant entities and return only the fields a query needs
- Keeping the semantic index separate from the graph on purpose, so records of all types can be indexed in different ways. The index is broken into the same granular structure per record (risk profiles, job history snapshots, active and resolved problems), refreshed nightly and rolled up weekly. A question like "have we seen this before?" finds records semantically, then takes their IDs into the graph for a rich picture within a couple of seconds
- Entity resolution in practice: matching inbound requests from portal emails and API connections to the right property, customer, call-out type, engineer and type of work, using social housing door-entry systems (blocks, units, and dozens or hundreds of doors) as the example. VH3 is above 90% first-pass recognition across about 20 sources, and the hierarchy in the graph helps decide which parent a site belongs to
- Human in the loop by design: automatic above roughly 80% confidence on each match, and below that a person picks from options VH3 has already built (such as door entry versus access control) in one click
- Sentinels: about 20 monitors in production, nearly pure graph reads that never touch an LLM, using a single Cypher query to walk a parent company's jobs and spot risks such as SLA breaches before they become apparent
- Ric's view that AI has been "a Trojan horse for automation": tools like Zapier were bridging these gaps for years, and the shift is that friction has dropped, which also made it practical to embed LLMs in programmatic flows
- Model routing (the right model for the job) and not relying on models for critical computation: do the looping, pagination and arithmetic server-side, and hand the model clean context with no null values or empty fields
- The "Cursor for field service" idea: give customers an enabling platform rather than a product they wait on a roadmap for, with domain experts increasingly able to build their own tools, and the risks that brings (the Dunning-Kruger effect, security holes, a breach being business-ending). Ric still advises keeping core systems with specialist platforms
- Buy versus build, data sovereignty and VH3's enterprise offering, where customers bring their own cloud and their own keys, with an expectation that more companies will move to self-hosted and open-weight models
- Provenance and observability: tracking the version, the model touched, token counts and cost across everything the platform does, so customers know what they are paying for, plus the warning that graphs are notorious for stale data and relationships if nobody maintains them
- Don't build your business on today's technology: advice Ric took from a talk by Piers Linney of ImplementAI, and his view that many 2024–25 AI startups went all-in on one stack and now find the ground has shifted
- Handling change over time (the host's closing question): pulling data from client systems about every minute, with loops that reconcile changed records, and every record carrying dates. Old records are never deleted. They become "maybe" with a score for why a newer one may be better, and a relationship is retired only when VH3 is confident another record should be used
- Knowledge base documents such as technical manuals and standards live mainly in the semantic index, are polled every 24 hours for changes and are permission-aware, and get graph relationships where parts are mentioned in job history
- Ric's goal for VH3: give customers enough controls that they eventually don't need VH3's professional services
- The Connected Startup's host plugged his Neo4j NODES 2026 talk on startup mistakes, which included thinking about entity resolution too late, since it can fragment your graph

## Links Mentioned

- **VH3 AI:** [vh3.ai](https://www.vh3.ai)
- **Neo4j Startup Program:** [neo4j.com/startup-program](https://neo4j.com/startup-program/)
- **Neo4j NODES** — Neo4j's annual virtual conference, where the host gave his talk on startup mistakes: [neo4j.com/nodes](https://neo4j.com/nodes/)
