# Grain MCP

The [[Grain]] MCP (Model Context Protocol) server that allows AI agents like Claude to interact with Grain's meeting data. Central to [[Grain Strategy]] of positioning meetings as the data layer for [[Agentic AI]].

## Update 2026-05-15 from [[2026-05-15_carlos-almonte-and-jeff-whitlock]]

### User feedback from [[Carlos Almonte]]

Carlos is an active MCP user who connected it to both his IDE and Claude web. Highlights:
- Bulk playlist organization by client domain works well and saves significant time
- Requested **read-level audit tools** for understanding sharing/access state of recordings
- Requested **write-level access management** to change permissions from within MCP
- Requested per-client automated security rules (e.g., lock down all recordings for domain X by default)

[[Jeff Whitlock]] confirmed these are directionally aligned with ongoing work:

> "We're actually working on rethinking our sharing model... the MCP has driven more demand for more context. We're trying to rethink how do we get more power so people can share more while still having trust that they're not going to share what they don't want to share."

Jeff also indicated settings/configuration from within the MCP is coming.

## Update 2026-05-15 from [[2026-05-15_agentic-workflows]]

[[Mike Adams]] demoed using the Grain MCP as a core input to his [[Knowledge Graph System]] vault workflow. Meeting transcripts flow into raw/, get compiled into wiki articles, and then inform project outputs like sales decks and marketing materials. Also proposed a shared [[Voice of the Customer]] vault powered by Grain MCP inputs across the team.

## Update 2026-04-23 from [[2026-04-23_pre-board-conversation-april-2026-1]]

### 15x growth signal

MCP weekly users grew ~15x with almost no investment. Docs were still the same "shitty documentation from June." Mike argued this should be the centerpiece of the board deck and Q2 strategy, not a footnote.

Mike: "If you told me we'd have a 15x growth in MCP when we didn't even do anything with it... people want it that bad. It's fucking awesome."

Jeff noted the connector approval with Anthropic is imminent and would be a massive unlock for distribution.

### Hosted developer docs

Jeff shipped hosted, agent-readable MCP and API docs at developers.grain.com. Previously in Notion. Now auto-deployed from markdown files.

## Update 2026-04-29 from [[2026-04-29_account-upgrade-audits]]

### MCP retention data

Amplitude analysis showed MCP tool calls have dramatically better retention than any in-app feature among paid users. Volume of 2,000 with strong week-over-week retention. This became a key argument for making MCP the centerpiece of growth strategy.

## Update 2026-05-01 from [[2026-05-01_demos]]

### Product features shipped

- In-app product announcement for MCP connector (replacing Intercom) — [[Jonny Andreola]]
- First-time user MCP footer directing users to connect — Andrew Clarkson
- Bulk actions with MCP-aware copy/export — [[Chris Naismith]]

## Update 2026-05-18 from [[2026-05-18_check-in-on-entity-md-docs-for-the-mcp]]

### Entity memory for MCP enrichment

See [[Entity Memory]]. The team (Jeff, [[Ygor Castor]], [[Shane Howley]]) aligned on building per-company markdown briefs that would be injected into MCP responses to provide cross-meeting context without requiring the LLM to search and synthesize from scratch each time.

## Sources
- raw/meetings/2026-05-15_carlos-almonte-and-jeff-whitlock.md
- raw/meetings/2026-05-15_agentic-workflows.md
- raw/meetings/2026-04-23_pre-board-conversation-april-2026-1.md
- raw/meetings/2026-04-29_account-upgrade-audits.md
- raw/meetings/2026-05-01_demos.md
- raw/meetings/2026-05-18_check-in-on-entity-md-docs-for-the-mcp.md
