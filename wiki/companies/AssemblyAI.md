# AssemblyAI

Transcription and speech AI provider. As of May 2026, [[Grain]] is moving all transcription from [[DeepGram]] to AssemblyAI.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### Grain migration

[[Ryan Johnson]] announced the switch:

> "We are actually going to be moving everything over to AssemblyAI."

Drivers:
- "Much better deal" on pricing compared to [[DeepGram]]
- Their "universal streaming pro" model tested as adequate after a second pass (first pass was not great)
- Recently released per-word speaker labels (previously per-turn only), improving [[Diarization]] granularity

### Diarization characteristics

- More willing to return `unknown` speaker labels than [[DeepGram]]
- Per-word speaker labels are new; [[Recall.ai]] passes through whatever granularity AssemblyAI provides

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
