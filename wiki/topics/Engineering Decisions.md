# Engineering Decisions

Technical decisions made by the [[Grain]] engineering team.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### Transcription provider switch: [[DeepGram]] to [[AssemblyAI]]

[[Ryan Johnson]] announced [[Grain]] is moving all transcription to [[AssemblyAI]]. Rationale:
- Better pricing deal
- AssemblyAI's "universal streaming pro" model quality is adequate after their second pass
- Per-word speaker labels (new from AssemblyAI) improve [[Diarization]] granularity

### Recall.ai SDK upgrade path

SDK 2.0.14 has a Safari screen capture bug. Team is implementing defensive measures on [[Grain]]'s side to allow upgrading despite the bug, since [[Recall.ai]] is shipping other important fixes. [[Tucker von Holten]] committed to fixing or gating the issue within a week.

### Diarization strategy

Evaluating [[Recall.ai]]'s experimental diarization fusion to potentially replace some of Grain's own diarization implementation. [[Ryan Johnson]]: "We love being able to delete code."

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
