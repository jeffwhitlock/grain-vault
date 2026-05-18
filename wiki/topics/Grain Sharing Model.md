# Grain Sharing Model

The system of defaults and permissions governing who can access [[Grain]] recordings, including team visibility, participant sharing, and per-recording controls. Actively being rethought as of May 2026.

## Update 2026-05-15 from [[2026-05-15_carlos-almonte-and-jeff-whitlock]]

### Current pain points (from [[Carlos Almonte]])

- **Team-wide default visibility is surprising.** Carlos did not realize all recordings were visible to everyone on his team. Had to contact [[Grain]] support to lock down every recording he owned.
- **Auto-send to participants is risky.** Default behavior sends recordings to all meeting participants. Carlos recounted an incident where internal post-meeting discussion was inadvertently shared with clients.
- **No granular per-client controls.** Carlos wants domain-based rules: recordings with Client X are always private, recordings with Client Y can be shared.

### Proposed improvements

Carlos suggested: notify participants by default, but require explicit permission for recording access. Also wants [[Grain MCP]] to expose audit and write capabilities for managing access.

### Strategic context

[[Jeff Whitlock]] confirmed a rethink is underway:

> "We're trying to rethink how do we get more power so people can share more while still having trust that they're not going to share what they don't want to share."

This is driven partly by [[Grain MCP]] adoption increasing demand for broader context sharing while maintaining trust.

> MERGE CANDIDATE: [[Grain Strategy]] — sharing model rethink is a strategic initiative.

## Update 2026-04-23 from [[2026-04-23_conversation-with-mike-feedback]]

### LLM-driven sharing via markdown rules

[[Mike Adams]] proposed replacing deterministic team-based sharing with heuristic-based LLM sharing. The model:
- Admin defines sharing rules in a markdown file (e.g., "one-on-ones are never shared," "all-hands are shared with everyone")
- An LLM agent interprets and applies rules, preserving reasoning traces
- When sharing goes wrong, the markdown file is updated so it doesn't happen again

> "What if you had markdown files in settings where these rules are defined... and it's just a set of heuristics and first principles for LLMs to follow to make judgment calls."

### Sensitivity classification

Meeting sensitivity could be classified automatically: personal, internal, external, highly sensitive. This would be an admin feature for business/enterprise plans.

### Default team proposal

Jeff proposed a quick win: create a default team where everyone is a member and everyone contributes. Add a simple rule: one-on-ones don't get shared. "That's two weeks of work."

### Flip the sharing paradigm

Instead of "nothing shared by default, add sharing rules to open up," flip to "everything shared by default, with a do-not-share list." This unlocks the [[Enterprise Expansion]] value of cross-meeting intelligence while reducing the cognitive load of configuring permissions.

## Update 2026-05-15 from [[2026-05-15_strategy-session-5-15-26-capture-and-sharing]]

### Capture-sharing integration

The capture settings redesign discussion (see [[Capture and Recording]]) includes a sharing dimension: different capture methods have different consent properties. Bot capture includes explicit meeting consent/disclosure; desktop capture does not. This affects auto-share rules downstream.

[[Mike Adams]] designed a flow-through model where capture method choices cascade into sharing behavior, surfaced in a unified settings page.

## Sources
- raw/meetings/2026-05-15_carlos-almonte-and-jeff-whitlock.md
- raw/meetings/2026-04-23_conversation-with-mike-feedback.md
- raw/meetings/2026-05-15_strategy-session-5-15-26-capture-and-sharing.md
