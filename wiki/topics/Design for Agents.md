# Design for Agents

The practice of structuring design systems, documentation, and workflows so that AI agents can implement UI effectively. Emerging discipline at [[Grain]] as of May 2026.

## Update 2026-05-15 from [[2026-05-15_agentic-workflows]]

### Current initiatives

[[Jeff Whitlock]] described work underway with contract designers:
- Building a `design.md` document with design principles and rules for how agents should implement designs
- Building **design tokens**: the design system codified into components and small chunks that agents can consume
- Setting up the design system so agents can use existing components, brand styles, and typography
- A contract designer is implementing the same approach at a public company with good results

### Shift from mockups to prototypes

Jeff noted the process is moving away from static Figma mockups toward building working prototypes. This changes the design workflow fundamentally.

### Pixel-perfect concern

[[Jonny Andreola]] raised a key tension: without a pixel-perfect Figma reference, where does polish happen?

> "Once you don't have that reference of pixel perfect, but we still want pixel perfect to be delivered to our customers, where does the polishing happen?"

Options discussed:
- In staging (risk: delays merges, can't ship until fixed)
- During development via screenshot feedback (risk: slow feedback loop)
- In follow-up PRs (acceptable but still a concern)

Jonny shared an example of spending extensive time debating "one pixel off" with a designer, noting the gap between what developers and designers consider acceptable.

### Architecture.md

[[Jonny Andreola]] is building an `architecture.md` file: a map of the codebase telling agents where to find things and where to place new things. Examples:
- "If you need a building block component, go to Sprout UI, avoid Grain UI because that's legacy"
- "If composing components for a specific page, go to this place"

Referenced the [[OpenAI]] harness engineering article on organizing agent instruction files (design.md, architecture.md, packs). Also mentioned [[Vercel]] documentation as a reference.

Current approach: add rules to root-level `agents.md` file, then extract into specialized files (design.md, architecture.md, business logic) once it gets too large.

## Sources
- raw/meetings/2026-05-15_agentic-workflows.md
