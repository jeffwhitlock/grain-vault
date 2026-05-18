# Capture and Recording

The fundamental data ingestion layer of [[Grain]]: how meetings get recorded via bots, desktop capture, or mobile. A persistent source of product complexity and strategic debate. Closely tied to [[Recall.ai]] dependency and [[Grain Strategy]].

## Update 2026-02-23 from [[2026-02-23_strategy-session]]

### Desktop capture reliability concerns

[[Ben DeMordaunt]] flagged desktop capture reliability as his "biggest heartburn":

> "I just posted that I wasn't able to get desktop capture working when I did my activation testing. I just tried all day. It said no audio detected."

[[Jeff Whitlock]] attributed much of this to [[Recall.ai]]'s complex architecture:

> "I'm just very convinced that it's the combination of Recall's complex architecture with our consumption of it... the surface area of things was just way more complicated than it needs to be."

The team discussed that Recall's SDK deep complexity is used to detect whether a user is in a meeting (for notepad display), which adds engineering cost that local capture doesn't need.

### Highlights gap on local captures

Ryan noted that highlights (a key API tool) are not available on local captures, creating workflow inconsistency.

## Update 2026-05-15 from [[2026-05-15_strategy-session-5-15-26-capture-and-sharing]]

### Capture method redesign

[[Mike Adams]] proposed flipping the settings model from organized-by-capture-method to organized-by-meeting-type with fallbacks:
- External meetings: preferred method + fallback
- Internal meetings: preferred method + fallback  
- Unscheduled: preferred method + fallback

[[Ryan Johnson]] pushed back on symmetric fallbacks: bot-as-fallback-for-desktop makes sense (bot can auto-join when desktop fails), but desktop-as-fallback-for-bot is unreliable since desktop capture requires specific conditions. He proposed using notifications instead for bot-to-desktop fallback.

[[Ben DeMordaunt]] noted from customer experience: "They always just fall into one bucket. It's either grain bot or it's grain desktop capture."

### Bot vs. desktop capture strategic direction

Jeff's long-term view: bots are under secular pressure from platform restrictions. Zoom and Google keep tightening. Desktop/local capture is better for activation. Granola's success with local-only reinforces this. But bots still have superior reliability for power users.

Mike: "Bots only die if the platforms force them to die... as an entrenched user, the reliability of bots is so much better."

### Duplication problem

A core tension: allowing both capture methods simultaneously creates duplicate recordings with double COGS. The team is not yet willing to invest in merge/deduplication engineering, so the capture settings force a binary choice that frustrates users.

## Sources
- raw/meetings/2026-02-23_strategy-session.md
- raw/meetings/2026-05-15_strategy-session-5-15-26-capture-and-sharing.md
