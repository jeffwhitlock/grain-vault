# Recall.ai

Meeting bot and SDK provider used by [[Grain]] for in-meeting audio/video capture and transcription integration. Key vendor relationship.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### SDK issues

- **Safari screen capture bug (2.0.14):** SDK was incorrectly requesting screen capture permission on Safari to determine active speaker. [[Tucker von Holten]] confirmed this is a bug and will be fixed or gated within a week. [[Ryan Johnson]] and [[Chris Naismith]] coordinating on defensive measures on [[Grain]]'s side to allow upgrading.
- **TypeScript typing gaps:** [[Chris Naismith]] requested typed events for SDK real-time events (currently `data` property is `any`). Tucker acknowledged this is needed but lower priority than stability fixes. [[Elliot Levin]] owns the SDK stability roadmap.

### Diarization fusion (experimental)

New experimental feature that fuses speaker label data from [[DeepGram]] and [[AssemblyAI]] transcription providers:
- Uses large historical dataset to flag when transcription provider labels are unreliable
- SDK-only for now (not affecting bots)
- May return `null` for words with no speaker confidence (when unknown feature is enabled)
- Should generally provide more information, not less
- [[Ryan Johnson]] testing to see if it can replace some of Grain's own diarization work

### Personnel change

[[Tucker von Holten]] departing Recall.ai. Recommended [[Elliot Levin]] as ongoing contact for SDK matters. Tucker had been working with [[Grain]] for about a year.

### Customer logging roadmap

Planning to build customer-facing logging for the SDK (currently only available for bots) and an MCP server for natural-language debugging. Would require auditing entire logging system.

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
