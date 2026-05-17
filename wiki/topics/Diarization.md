# Diarization

Speaker identification and labeling in meeting transcripts. A core quality driver for [[Grain]]'s transcript accuracy and a current area of active investment.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### Recall.ai diarization fusion

[[Recall.ai]] shipped an experimental diarization feature for the SDK that fuses speaker labels from transcription providers ([[DeepGram]], [[AssemblyAI]]):
- Uses historical recording data to flag when provider labels are unreliable
- May return `null` speaker labels when confidence is low (unknown feature)
- Requires post-processing: "If we're in a sentence, let's just attribute it to the other word in the sentence"
- SDK-only, not affecting bots during beta
- [[Ryan Johnson]] evaluating whether this can replace some of [[Grain]]'s own diarization work

### Provider differences

- [[DeepGram]] has had streaming diarization longer; tends to attribute unknown words to previous speaker rather than returning unknown
- [[AssemblyAI]] "much more willing to return unknown than DeepGram"
- AssemblyAI released per-word speaker labels (previously per-turn only); [[Recall.ai]] passes through whatever granularity the provider returns

### Grain moving to AssemblyAI

[[Ryan Johnson]] announced [[Grain]] is switching from [[DeepGram]] to [[AssemblyAI]] for transcription:

> "We are actually going to be moving everything over to AssemblyAI."

Reasons: better pricing deal, and their streaming pro model ("universal streaming pro") tested as "decent enough" after a second pass.

### Voice Signatures

Separate from Recall.ai work, [[Jeff Whitlock]] mentioned [[Grain]] is building [[Voice Signatures]] for speaker identification independent of calendar/Zoom matching. Useful for in-person meetings, shared computers, and unscheduled meetings.

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
- raw/meetings/2026-05-15_carlos-almonte-and-jeff-whitlock.md
