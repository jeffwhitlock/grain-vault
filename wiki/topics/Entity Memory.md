# Entity Memory

A project to create persistent, per-entity markdown briefs (companies, contacts) that enrich [[Grain MCP]] responses with cross-meeting context. Part of [[Grain]]'s strategy to be more than raw transcript storage.

## Update 2026-05-18 from [[2026-05-18_check-in-on-entity-md-docs-for-the-mcp]]

### Strategic rationale

[[Jeff Whitlock]] framed the project as answering why Grain exists as a middle layer:

> "This project is our attempt to figure out what is Grain beyond just raw storage of transcripts... why does a company care about having Grain in the middle layer. Well, it's because we can do enrichment."

The unique data Grain has is the history of conversations. The hypothesis: LLMs are still not good enough at fully using a large corpus of raw transcripts, so condensed entity briefs provide significant value.

### V1 design decisions

[[Ygor Castor]], [[Shane Howley]], and Jeff aligned on:
- Start with **company-level entities** only (not per-person)
- Store as a **single markdown per entity**, updated after each meeting
- Use **condensed outputs** (notes + action items) not full transcripts to control cost
- **Bootstrap** by processing first meeting + last N meetings when a new meeting triggers entity creation
- Avoid knowledge graph complexity. Jeff: "I really don't want to do the graph database. We're not trying to build a graph database here. We're just trying to do briefs."
- Consider storing diffs for version history, but don't over-engineer

### Company brief contents

Shane pushed for clarity on what goes in: company info, stakeholders, project threads, outstanding commitments, action items. Firmographic data from People Data Labs could seed the top-level blurb.

> MERGE CANDIDATE: [[Knowledge Graph System]] — Entity Memory is the product implementation of concepts discussed in Knowledge Graph System.

## Sources
- raw/meetings/2026-05-18_check-in-on-entity-md-docs-for-the-mcp.md
