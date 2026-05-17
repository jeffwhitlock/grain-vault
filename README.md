# Jeff's Knowledge Graph Vault

Personal Karpathy-style knowledge graph. LLM-curated wiki as an alternative to vector embeddings for long-term memory.

## How to use

### Daily
- `daily-brief` skill for morning context
- Meetings auto-ingest via the webhook server
- `compile-raw` end of day or weekly

### When producing something
- cd into projects/<project>
- Agent reads wiki/ for context
- Output goes to projects/<project>/ or external destination

## Architecture

raw/ → compile-raw → wiki/ → projects/

## Ingestion

- **Primary:** Local webhook server + ngrok listens for Grain `recording_added` event, fetches transcript via Grain workspace API, writes to raw/meetings/. Server source: `~/Documents/Claude/Projects/Create Knowledge Graph System/server/`.
- **Backfill:** `backfill-grain-meetings` skill uses the Grain MCP to pull historical meetings on demand.

## Skills

- `compile-raw` — extracts entities, claims, and decisions from raw/ into wiki/ articles
- `backfill-grain-meetings` — manual historical pull from Grain
- `daily-brief` — morning context: calendar, wiki changes, open projects

## Running the webhook server

```bash
cd ~/Documents/Claude/Projects/Create\ Knowledge\ Graph\ System/server
npm run dev

# In another terminal:
ngrok http 3000
# Update the Grain webhook URL if the ngrok URL changed
```

## Decisions log

| Date | Decision | Rationale |
|---|---|---|
| 2026-05-17 | Vault at /Users/Jeff/vault/ | Home root, no spaces, not in iCloud |
| 2026-05-17 | Webhook server (not MCP polling) as primary ingestion | Real-time arrival, durable; matches Mike's setup |
| 2026-05-17 | Hosting: local + ngrok | Jeff's preference; simplest path |
| 2026-05-17 | Sync mode: local-only | Server runs on same machine, direct file write |
| 2026-05-17 | Listen for recording_added only | recording_updated fires on manual edits (noise) |
| 2026-05-17 | Superpowers over GSD | Lower overhead for small frequent tasks |

## Open questions

- Cloud-hosted vault so it runs without laptop on?
- Team-level voice-of-customer vault (Mike to propose)
- Cost monitoring on compile runs
- ngrok static domain for persistent webhook URL

## When to retire this

Mike said he might throw his out in 2-3 months. Same posture here. If after 6 weeks the outputs aren't noticeably better than baseline, kill it and write a postmortem.
