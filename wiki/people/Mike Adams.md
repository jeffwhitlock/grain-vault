# Mike Adams

Chairman of [[Grain]]. Built the original Karpathy-style [[Knowledge Graph System]] that this vault is modeled on.

## Update 2026-05-15 from [[2026-05-15_agentic-workflows]]

### Vault demo at Agentic Workflows meeting

Demoed the full vault system to the [[Grain]] engineering team. Key elements shown:
- Webhook-powered raw ingestion (meetings split by attended vs. not attended)
- Compile-raw skill processing into wiki articles
- Account analysis framework using multiple APIs and MCPs for deep customer research
- RAM Construction sales deck generated entirely from the framework, presented to prospect the day prior. Deck used the PPTX skill and was uploaded to Google Drive via GWS CLI.

> "That framework both is informed by the wiki and then also contributes back into the wiki, and it feels like this kind of represents a slight representation of my brain that just generally makes all of my outputs better and smarter."

### Slack Zero workflow

Built a "Slack Zero" skill that processes all Slack messages through the MCP. The MCP won't mark messages as read, but the skill helps him process messages one by one and then execute actions in the actual Slack UI.

### Voice of the Customer vault proposal

Proposed a shared [[Voice of the Customer]] vault as a team-wide asset:

> "It'd be really interesting to create a processing flow like this, especially that's automated and ideally remote hosted, that is just creating a voice of the customer vault."

Vision: aggregate inputs from support channels, sales calls, and research into a wiki organized by themes and topics. Any query about customer needs could point to this vault for context.

[[Jeff Whitlock]] endorsed it: "Let's build it."

### Claude Design workflow

Used Claude Design for visual frameworks and infographics. Workflow: remix [[Jeff Whitlock]]'s Claude Design files, produce infographic versions of complex frameworks. Found it useful for clarifying his own thinking and communicating to others. Works within [[Grain]]'s design system (set up by [[Chris Naismith]]).

### Mental model for tool selection

When asked by [[Ben DeMordaunt]] how to choose between Claude Code, Claude Design, and Desktop:
- **Vault/Claude Code**: when it needs a lot of context, local processing, libraries, or plugins
- **Claude Design**: UI-heavy work, visual frameworks, infographics
- **Superpowers framework**: replaced GSD ("super bloated") for project planning; breaks work into parts with plans for each

## Update 2026-04-23 from [[2026-04-23_conversation-with-mike-feedback]] and pre-board conversations

### Strategy clarity feedback

Identified Jeff's translation gap as a core issue: Jeff sees strategy clearly in conversation but struggles to codify it in docs and communicate it to the team and market. Offered to collaborate on a strategy doc over two weeks.

### Sharing model via markdown rules

Proposed a paradigm shift: instead of deterministic team-based permissions, use LLM-driven heuristic sharing based on markdown rule files. Admins would define sharing rules in natural language. An agent would interpret and apply them, preserving reasoning traces.

### PQL forensic audit approach

Conducted hands-on Vistify account audit in [[2026-04-29_account-upgrade-audits]]. Diagnosed the entire self-serve upgrade flow as incoherent. Drove urgent framing: "The heavens parted and we have a chance again. We can't jog into it. We have to run into it."

### EdTech venture consideration

Candidly shared he's exploring a new EdTech startup through a venture studio (Gates Foundation grant). Focused on cognitive offloading in education. Estimated July as earliest incorporation. Said the Grain CEO possibility would rank above EdTech if the arrangement worked for both him and Jeff.

## Sources
- raw/meetings/2026-05-15_agentic-workflows.md
- raw/meetings/2026-04-23_conversation-with-mike-feedback.md
- raw/meetings/2026-04-23_pre-board-conversation-april-2026-1.md
- raw/meetings/2026-04-23_pre-board-conversation-april-2026-2.md
- raw/meetings/2026-04-29_account-upgrade-audits.md
