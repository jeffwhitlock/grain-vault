# Vault Agent Instructions

You are operating inside Jeff Whitlock's personal knowledge graph vault. The system is modeled on Andrej Karpathy's LLM-curated wiki concept.

## The pipeline

raw/ → compile-raw skill → wiki/ → projects/ produce outputs that reference wiki/

- **raw/** is intake. Files land here from webhooks, web clippings, manual drops. Never edit files in raw/ except to mark them processed.
- **wiki/** is the curated knowledge graph. Articles use Obsidian `[[wiki-links]]` to connect. The compile-raw skill is the primary writer; you may edit manually but prefer compile.
- **projects/** is active work. Each subfolder is its own Claude Code project with its own CLAUDE.md. Projects READ from wiki/ for context, WRITE artifacts back to projects/ or to external destinations (Drive, Slack, etc.).

## Rules for any agent

1. **Always read wiki/index.md and relevant wiki/ articles before producing output.** The wiki is the context layer. Skipping it defeats the system.
2. **Cross-link liberally.** Any wiki article that mentions a person, company, project, or topic should use `[[Name]]` syntax. The graph value is in the links.
3. **Minimize interpretation.** Quote sources where claims are strong. Paraphrase where weak. Flag uncertainty.
4. **Append, do not overwrite.** When updating an existing wiki article, add a new dated section. Preserve prior content.
5. **Surface conflicts, do not resolve them silently.** If two raw inputs disagree, write both and flag.
6. **Token cost matters.** Compile runs can burn 100k+ tokens. Be deliberate about scope.

## Tool preferences

- pptx skill for decks
- docx skill for memos
- xlsx skill for data
- Grain MCP for meeting access if not webhook-ingested

## Voice when writing for Jeff

- Direct, concise, no preambles or filler
- Structured (headers, bullets, tables) for non-prose; prose for reports/explanations
- No em dashes
- Quantify when possible
- Skip AI disclaimers
