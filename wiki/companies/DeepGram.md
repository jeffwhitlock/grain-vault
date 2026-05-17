# DeepGram

Speech AI and transcription provider. Previously [[Grain]]'s primary transcription provider; being replaced by [[AssemblyAI]] as of May 2026.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### Grain departing

[[Ryan Johnson]] confirmed [[Grain]] is moving all transcription to [[AssemblyAI]] due to better pricing. DeepGram had been used for its streaming [[Diarization]] capabilities.

### Diarization behavior

- Has had streaming diarization longer than [[AssemblyAI]]
- Tends to attribute unknown words to previous speaker rather than returning unknown labels
- [[Recall.ai]]'s fusion system accounts for these provider-specific behaviors

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
