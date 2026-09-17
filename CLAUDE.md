# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

A public catalog for **The Connected Startup**, a monthly podcast by Neo4j about founders who used graph technology to solve hard problems. Episodes air live every 3rd Thursday at 12pm Eastern.

## Structure

- `README.md` — show overview, schedule, and the episode table
- `episodes/` — one markdown file per episode, named `ep{NNN}-{guest-slug}-{company-slug}.md`

## Episode Files

Each episode file follows this structure:

1. Title, air date, guest name + role
2. **Watch & Listen** — platform links (YouTube, LinkedIn — only include platforms actually used)
3. **About {Guest Name}** — bio
4. **About {Company}** — description + website and GitHub links if available
5. **Episode Summary** — 2–3 sentence summary
6. **Topics Covered** — bullet list
7. **Links Mentioned** — any resources the guest referenced on air

## Show Flow

Every episode follows the same structure. Use it when creating notes for the show host and when structuring episode summaries from the transcript:

1. **Introduction**
2. **Stage 1: The Problem**
3. **Stage 2: The Graph Moment** — the transition from Stage 1 to Stage 2 is always the question *"Describe the moment you realized a graph was the right tool."*
4. **Stage 3: What Made It Possible and Where Are You Going Now**
5. **Closing**

## README Episode Table

- Columns: `#`, `Guest`, `Company`, `Air Date`, then one column per platform (YouTube, LinkedIn)
- The **Company** column should always link to the company's website (e.g. `[Papr.ai](https://papr.ai)`)
- Platform links use shields.io badges: YouTube (red), LinkedIn (0077B5)
- Leave platform cells empty when that episode wasn't broadcast on that platform

## Adding a New Episode

1. Create `episodes/ep{NNN}-{guest-slug}-{company-slug}.md` from the structure above
2. Add a row to the episode table in `README.md`
3. Commit and push — the remote is `https://github.com/neo4j-field/connected-startup-podcast.git`
