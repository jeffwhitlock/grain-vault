# Grain Strategy

[[Grain]]'s strategic direction and competitive positioning. The company is profitable and growing, with a focused bet on being the meeting data layer for [[Agentic AI]].

## Update 2026-05-15 from [[2026-05-15_carlos-almonte-and-jeff-whitlock]]

### Vision and positioning

[[Jeff Whitlock]] articulated the vision clearly:

> "Meetings are the interface for work in the world of agentic AI because it's how humans share ideas. It's how decisions are made. It's how alignment happens."

Three pillars of value:
1. **Universal capture** — more investment coming to make capture easier and broader
2. **Data enrichment** — [[Knowledge Graph System]] for cross-meeting context, [[Voice Signatures]], better [[Diarization]]
3. **Agent-ready data** — structured data delivered efficiently to agents via [[Grain MCP]]

### Competitive landscape

- **[[Fathom]]**: Closest competitor. Bigger, growing faster. Better business decisions but Jeff believes Grain has the better product. Fathom still focused on in-product experiences (deals, dashboards). Grain betting on agent-first data layer.
- **[[Fireflies]]**: Enterprise-focused, sells to IT buyers. Product is complicated with too many features, not as well designed.
- **Otter**: Strategy unclear, has "switched strategies a few times in the last two years." No video capability.

### Differentiation

> "The UI is there to help ensure that you're capturing and you're configuring things. And occasionally watch videos. But the real value is making it super easy so structured and rich data can be given efficiently to agents to do the work. I'm not sure they're fully embracing that strategy as much as we are." — [[Jeff Whitlock]] on [[Fathom]]

### Sharing model rethink

Active initiative to redesign the [[Grain Sharing Model]]. Driven by [[Grain MCP]] adoption increasing demand for broader context sharing while maintaining trust and security.

## Update 2026-02-23 from [[2026-02-23_strategy-session]]

### Strategic simplification push

First strategy session. Team aligned on the need to simplify personas, workflows, and use cases. Key themes:

- **Google Meet/Gemini threat**: The only consistently visible threat in churn data. Increasing but not at "five alarm fire level."
- **Fathom displacement**: [[Grain]] is winning over [[Fathom]] customers, primarily on the strength of offering both desktop and bot capture.
- **Persona debate**: The team debated horizontal vs. vertical positioning. [[Jake]] described being in "an awkward middle." Jeff explored a persona called the "productivity hacker" or "nontechnical automator" who wants meeting data to power workflows.
- **Workflow gaps**: Many half-built features (trackers, stories, integrations) that need to be either finished or killed. [[Ryan Johnson]] pushed for understanding the top 3 workflows.
- **Data-out vs. in-product**: The team debated whether to invest in making notes perfect inside Grain or getting raw/enriched data out to external AI tools. Consensus leaned toward data-out with in-meeting capture (notepad) as the stickiness layer.

> "I've seen it a ton lately where people just, like, I want the data in my AI tools." — [[Jeff Whitlock]]

### Decision: deprecate Deals feature

The group aligned on deprecating the Deals page. Mike: "Deals is essentially dead." Ben: "Deals doesn't come up in sales anymore." Retention data later confirmed near-zero 12-week retention.

## Update 2026-03-02 from [[2026-03-02_strategy-session-agentic-workflows]]

### Agentic workflows direction

Jeff shared a strategy doc on agentic workflows. Key discussions:

- [[Ryan Johnson]] argued to focus on proving value for power users first rather than solving installation friction. "Prove that out for motivated power users. And then once we've proven the value is there, then you can worry about how to get it more easily installed."
- [[Mike Adams]] noted the word "video" appeared zero times in the strategy doc. He argued video content (especially screen shares) has enrichment value via multimodal understanding, but it is supplementary, not core value.
- The team discussed that MCP loads everything into the main chat context, making it inefficient. Claude Code's sub-agent pattern produces better results by searching and summarizing before feeding back to main context.
- Mike advocated a low-investment V1: save transcripts as markdown files locally in a grain folder, publish a Claude skill for using them. "Just storing a copy as a markdown file in a grain folder in their documents folder."

### Transcript format spec

Jeff introduced a "Grain Meeting Transcript Format Spec" for LLM-optimized transcript output. Team was enthusiastic. Mike: "Our MCP server right now swapped out the way we do transcripts... it would be so much better."

## Update 2026-03-04 from [[2026-03-04_strategy-review-adapting-to-market-changes]]

### Assumptions audit

Jeff reviewed the assumptions underlying the previous strategy:
1. **Consistently meeting sales MMRs** — lagged due to needing core notetaking investment
2. **Decision makers wanting a single notetaker** — weakened by Gemini and Zoom Notes commoditizing basic capabilities
3. **Win with sales, spread to org** — still happening but the "spread" assumption weakened by platform-native alternatives

Jeff and Mike aligned that the consultant ICP exploration was the right divergent process but glad they didn't commit to it.

## Update 2026-04-23 from [[2026-04-23_conversation-with-mike-feedback]]

### Strategy clarity as priority one

Mike identified Jeff's core gap: translating strategic vision into clear, simple documentation.

> "You struggle to articulate a vision and make it clear in a doc. I think you see it, feel it, when we talk. And then there's just this translation to the team. And then even more so to the market."

They aligned on writing a strategy doc together over two weeks at the "principle and policy level, not the feature project level."

### System of record for agents

Jeff and Mike converged on "enterprise meeting system of record for agents" as the positioning. Mike suggested adding "enterprise" to emphasize company-wide value.

### Sharing model innovation

Mike proposed an LLM-driven sharing model using markdown rules files instead of deterministic team-based permissions. Key insight: meeting types and sensitivity can be classified by LLMs, removing the need for complex manual team configuration.

> "What if you had markdown files in settings that were these rules defined... and it's just a set of heuristics and first principles for LLMs to follow to make judgment calls."

## Update 2026-05-01 from [[2026-05-01_demos]]

### All-hands strategy presentation

Jeff presented the new strategy to the full team. Key frames:

Evolution of Grain's value prop:
1. Meeting library / collective intelligence → didn't work (people didn't watch videos)
2. AI notes → good bump but ephemeral, no compound value
3. **Enterprise meeting system of record for AI agents** → current bet

> "The new workflow is enriched queryable organization-wide meeting context that matches the context of the work you're actually doing and flows easily into the AI tools where the work is happening."

Explicitly chopped off sales managers as a target persona. New buyer targets: ops leaders, IT, chief of staff, CEO.

ICP: still 50+ person companies, meeting-heavy industries (SaaS primary), nudging upmarket. Horizontal on industry but focused on companies where meetings are primary input to work.

## Sources
- raw/meetings/2026-05-15_carlos-almonte-and-jeff-whitlock.md
- raw/meetings/2026-02-23_strategy-session.md
- raw/meetings/2026-03-02_strategy-session-agentic-workflows.md
- raw/meetings/2026-03-04_strategy-review-adapting-to-market-changes.md
- raw/meetings/2026-04-23_conversation-with-mike-feedback.md
- raw/meetings/2026-05-01_demos.md
