# Jonny Andreola

Frontend engineer at [[Grain]]. Leading efforts on agent-oriented codebase documentation and [[Design for Agents]] infrastructure.

## Update 2026-05-15 from [[2026-05-15_agentic-workflows]]

### Architecture.md initiative

Building an `architecture.md` file to map the [[Grain]] codebase for AI agents. The goal is a guide that tells agents where to find components and where to place new ones. Has started a Slack thread with a draft for the frontend.

Key architectural rules being codified:
- Use Sprout UI for building block components (Grain UI is legacy)
- Component composition follows specific directory patterns
- Agent rules currently live in a root-level `agents.md` and will be extracted into specialized files as they grow

### Pixel-perfect design concern

Raised the tension between removing pixel-perfect Figma references and still expecting pixel-perfect delivery. Concerned about delays if polish happens in staging or via screenshot feedback loops during development.

> "We don't provide a pixel perfect reference, but we expect to deliver one. If you leave designers to come up with this pixel perfect, it's going to be off always a little bit."

Referenced spending significant time debating a single pixel with a designer, illustrating the gap between developer and designer standards.

### References

Cited [[OpenAI]]'s harness engineering article and [[Vercel]]'s documentation as models for organizing agent instruction files.

## Sources
- raw/meetings/2026-05-15_agentic-workflows.md
