# Chris Naismith

Engineer at [[Grain]] working on SDK integration with [[Recall.ai]]. Focused on transcript data handling, typing, and SDK reliability.

## Update 2026-05-15 from [[2026-05-15_grain-recall-ai-sync]]

### SDK typing request

Requested TypeScript types for real-time SDK events, particularly the transcript data event where `data` is currently typed as `any`. [[Tucker von Holten]] acknowledged the need but said stability fixes are higher priority.

### Diarization questions

Asked about per-word vs per-turn speaker labels from [[AssemblyAI]]. Confirmed [[Recall.ai]] passes through whatever granularity the provider gives.

Noted that [[DeepGram]] and [[AssemblyAI]] handle unknown speakers differently: DeepGram rolls unknowns into the previous speaker, while AssemblyAI has its own turn-based issues.

### Customer communication

Raised the need for better feedback loops on SDK bug fixes: when [[Recall.ai]] ships a fix, [[Grain]] needs to know which recordings were impacted so they can close the loop with affected customers.

## Sources
- raw/meetings/2026-05-15_grain-recall-ai-sync.md
