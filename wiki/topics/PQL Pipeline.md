# PQL Pipeline

The Product Qualified Lead pipeline is [[Grain]]'s emerging framework for converting self-serve signups into paying customers by tracking product engagement signals rather than relying solely on inbound sales inquiries. Central to Q2 2026 strategy under [[PLG Growth]].

## Update 2026-04-29 from [[2026-04-29_account-upgrade-audits]]

### Core problem diagnosis

[[Mike Adams]] conducted a forensic audit of the Vistify account and concluded the current model is fundamentally incoherent, not just unoptimized:

> "This is not an optimization. We don't have a coherent model. We have a model. It's just unbelievably incoherent."

[[Ben DeMordaunt]] agreed: "I would even be more harsh and say we don't have a model. We have a bunch of piecemeal things that have agglomerated together over a long period of time."

Key findings from the Vistify audit:
- Only 4 of 17 workspace users were active, all on the revenue side
- Pricing and packaging is confusing with unclear upgrade value
- No automated outreach around trial expiry
- No account-level dashboard for tracking engagement
- Competitors (Fireflies, Otter) are aggressively growth-hacking while Grain is neither aggressive nor coherent

### Framework: qualification signals vs. stages

Mike proposed separating two dimensions:
1. **Qualification signals** — firmographic attributes (company size, domain) plus behavioral attributes (MCP connected, integrations set up, pricing page viewed, workspace expanded)
2. **Qualification stages** — linear progression: Signup → Trial Started → Activated → Engaged → Auto Extended → SQL Created → Closed Won/Lost

> "They can happen in any order. The stages that we've talked about are the big stages. And now these are little micro interactions that are really high signal."

### Trial extension as a conversion tool

Rather than extending default trial length, the group aligned on using staged trial extensions as engagement levers:
- Auto-extend trials for engaged, qualified accounts
- Communicate the extension as a gift: "Looked like you could use a little more time"
- Use the extension touchpoint to establish contact and move to SQL

### Feature retention data (kill candidates)

Amplitude retention analysis showed:
- **Deals page**: 12-week retention drops to 1%. [[Ben DeMordaunt]]: "Deals doesn't come up in sales anymore. We don't need it."
- **Insights page**: 12-week retention also near zero. 4,000 initial views, 9 users at week 10.
- **Coaching**: Slightly better initial engagement than deals, but same atrophy to single digits by week 12
- **MCP tool calls**: Dramatically better retention than any in-app feature among paid users. Volume of 2,000 with strong week-over-week retention.

## Update 2026-04-30 from [[2026-04-30_pql-follow-up-discussion]]

### Pipeline design in HubSpot

[[Mike Adams]], [[Ben DeMordaunt]], and [[Jeff Whitlock]] designed a PQL pipeline with stages:
- Signup → Qualified Trial Started → Activated → Trial Engaged → Auto Extended → SQL Created

The auto-extension is the critical intervention point. Once an account reaches auto-extended, it creates a deal in the existing sales pipeline.

### Attribute vs. stage separation

Jeff pushed for cleanly separating three dimensions:
1. Firmographic attributes (company size, enriched data)
2. Behavioral signals (MCP connected, integrations, pricing page viewed)
3. Journey-based triggers (trial ending, workspace expanded)

### AI adoption levels framework

Jeff outlined a customer education framework tied to PQL outreach:
- Level 1: Reading AI-generated notes
- Level 2: Per-meeting transcript analysis in external AI
- Level 3: MCP connected, cross-meeting analysis
- Level 4: Automated agents doing scheduled work from meeting data

> "We want to help you get to this level. Pull you forward into the new AI way of working."

## Update 2026-04-30 from [[2026-04-30_pql-playbook-follow-up-w-ben-and-jeff]]

Jeff clarified to Ben the overall narrative shift needed: "We are changing the narrative from here is this thing that you get some notes from... to this is a new way of working. We are the enterprise meeting system of record for you to have meetings and then have AI do your work."

Ben acknowledged a gap in his understanding: "It's just been a little bit hazy on this shift in being a meeting system of record for AI."

Jeff committed to codifying the messaging further and presenting the new paradigm at the company all-hands.

## Sources
- raw/meetings/2026-04-29_account-upgrade-audits.md
- raw/meetings/2026-04-30_pql-follow-up-discussion.md
- raw/meetings/2026-04-30_pql-playbook-follow-up-w-ben-and-jeff.md
