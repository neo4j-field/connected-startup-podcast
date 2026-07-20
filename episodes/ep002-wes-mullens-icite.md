# Episode 002 — Wes Mullens, Icite

**Air date:** July 16, 2026  
**Guest:** Wes Mullens, Founder & CEO, Icite

---

## Watch & Listen

- **YouTube:** [Watch on YouTube](https://www.youtube.com/watch?v=2C_N_UeMsa4)
- **Twitch:** [Watch on Twitch](https://www.twitch.tv/videos/2821439121)

---

## About Wes Mullens

Wes is the founder and CEO of Icite. Before founding the company, he was CTO at one of the largest managed detection and response (MDR) providers, where running security operations at scale showed him that identity had quietly become the attack surface no SIEM, EDR, or cloud tool could fully see.

---

## About Icite

Icite is a cloud-based cybersecurity company focused on Advanced Identity Threat Detection and Response (ITDR). Where SIEMs and EDRs see events and endpoints, Icite sees identity — resolving who a user is across every IDP, SaaS app, and local account in the environment, then using that graph to power detections no traditional security tool can match.

- **Website:** [icite.io](https://icite.io/)

## Episode Summary

Wes walks through how Icite built a three-database architecture — PostgreSQL for structured data, ClickHouse for time series, and Neo4j as the source of truth for identity resolution. The core problem: 90% of breaches tie back to an identity, but a SIEM can never fully resolve who a user is across dozens of IDPs and SaaS apps where the same person appears under different usernames, email formats, and provisioning paths. Graph makes that resolution fast, and it makes the detections that depend on it possible.

He also covers why the team migrated from AWS Neptune to Neo4j (deep graph traversal at scale, the GDS library, and Aura's managed hosting), how AI agents writing Cypher queries instead of SQL cut token costs by nearly an order of magnitude, and where Icite is headed next: permission-structure analysis, blast radius scoring, and tracking the identities of AI agents themselves.

---

## Topics Covered

- Why identity became the primary attack surface — and why SIEMs, EDRs, and cloud tools can't fully see it
- The three-database architecture: PostgreSQL (structured) + ClickHouse (time series) + Neo4j (identity graph)
- Identity resolution: mapping one person across multiple IDPs, SaaS apps, local accounts, and SSO gaps
- Moving from AWS Neptune to Neo4j — deep graph traversal, the GDS library, and performance at scale
- Neo4j Aura managed service as a force multiplier for a small startup team
- How the detection engine uses graph traversal to combine identity, permissions, and activity in a single query
- AI agents writing Cypher via a custom tool — token efficiency vs. equivalent SQL (25k vs. 200k tokens per query)
- The Icite MCP server and graph as a natural fit for agentic infrastructure
- Non-human identities: tracking AI agent permissions and detecting drift vs. human access
- What's next: attack path analysis, blast radius scoring, and posture based on permission structures
