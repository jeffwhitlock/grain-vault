# Tucker von Holten

Engineer at [[Recall.ai]] who has been the primary point of contact for the [[Grain]] SDK integration. Departing Recall.ai as of May 2026.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### Safari screen capture bug

Confirmed the Safari screen capture permission prompt in SDK 2.0.14 is a bug:

> "This is absolutely a bug. Like I just want to be clear from our end that this is not the behavior."

Committed to either fixing the underlying issue within a week or gating the behavior so it does not request the permission when not granted.

### Customer logging and MCP server

Discussed plans to improve customer-facing logging for the SDK (not just bots):
- Goal: reveal more information to customers for debugging
- Building an MCP server that, combined with better logging, would let customers describe problems in natural language rather than submitting recording IDs
- Would be "a little bit of an overhaul" to audit the entire logging system for what should be customer-visible

### Departure from Recall.ai

Announced he is leaving [[Recall.ai]]:

> "Not to drop a bomb, but I am also heading out of Recall. All positives. But I just wanted to show you guys as well. I've been working with you guys for about a year."

Recommended following up with [[Elliot Levin]] for ongoing SDK matters.

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
