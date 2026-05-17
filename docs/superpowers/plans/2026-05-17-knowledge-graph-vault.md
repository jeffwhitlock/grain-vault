# Knowledge Graph Vault Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Stand up Jeff's personal Karpathy-style knowledge graph system — an LLM-curated wiki fed by Grain meetings, web clippings, and manual drops, with Obsidian as the viewer and Claude Code skills as the processing layer.

**Architecture:** Raw inputs land in `raw/` via webhook or manual drop. The `compile-raw` skill extracts entities, claims, and decisions into `wiki/` articles with Obsidian `[[backlinks]]`. Projects in `projects/` read the wiki for context when producing artifacts. Grain meetings are the primary input, ingested by a local Express server receiving webhooks via ngrok.

**Tech Stack:** Node.js + Express (webhook server), Obsidian (viewer), ngrok (tunnel), Grain workspace API, Claude Code skills (compile-raw, daily-brief, backfill), Git + GitHub (version control).

**Decisions locked in:**

| Item | Decision | Rationale |
|---|---|---|
| Vault location | `/Users/Jeff/vault/` | Home root, no spaces, not in iCloud |
| Webhook hosting | Local + ngrok | Simplest path, Jeff's preference |
| Sync mode | Direct local write | No git-push needed since server runs on same machine |
| Webhook event | `recording_added` | Fires post-processing; includes AI fields proving transcript is ready |
| Server location | `/Users/Jeff/Documents/Claude/Projects/Create Knowledge Graph System/server/` | Separate from vault |
| Framework | Superpowers skills, not GSD | Lower overhead for small frequent tasks |

---

## File Structure

### Vault (`/Users/Jeff/vault/`)

```
/Users/Jeff/vault/
├── .claude/
│   ├── CLAUDE.md                                    # vault-level agent instructions
│   └── skills/
│       ├── compile-raw/SKILL.md                     # the brain — raw/ → wiki/
│       ├── backfill-grain-meetings/SKILL.md         # manual historical pull via Grain MCP
│       └── daily-brief/SKILL.md                     # morning context loader
├── raw/
│   ├── meetings/                                    # auto-populated from Grain webhook
│   ├── clippings/                                   # web articles via Obsidian Web Clipper
│   └── inbox/                                       # manual drops (emails, PDFs, notes)
├── wiki/
│   ├── index.md                                     # top-level index, maintained by compile
│   ├── topics/                                      # concept articles
│   ├── people/                                      # person articles
│   ├── companies/                                   # company articles
│   └── projects/                                    # project/initiative articles
├── projects/                                        # active work that reads from wiki/
├── scripts/                                         # utility scripts
├── decisions/                                       # decision records
├── docs/superpowers/plans/                          # this plan lives here
├── .gitignore
└── README.md
```

### Webhook Server (`/Users/Jeff/Documents/Claude/Projects/Create Knowledge Graph System/server/`)

```
server/
├── package.json
├── .env                      # GRAIN_API_KEY, WEBHOOK_SECRET, VAULT_PATH, PORT (gitignored)
├── .env.example              # checked in, documents required vars
├── .gitignore
├── src/
│   ├── index.js              # Express app + route handler
│   ├── grain.js              # Grain API client: fetchRecording(id), fetchTranscript(id)
│   ├── writer.js             # markdown writer + frontmatter formatter
│   └── verify.js             # webhook signature verification (HMAC-SHA256)
└── README.md
```

---

## Task 1: Seed the wiki and initialize git

**Files:**
- Create: `wiki/index.md`
- Create: `wiki/topics/ICP Validation.md` (and 7 other topic stubs)
- Create: `wiki/people/Mike Adams.md` (and 5 other people stubs)
- Create: `.gitignore`

- [ ] **Step 1: Create wiki/index.md**

```markdown
# Wiki Index

This is the top-level index of Jeff's personal knowledge graph. The compile-raw skill maintains this file. Add new top-level topics here as they emerge from raw inputs.

## Topics
- [[ICP Validation]]
- [[PLG Growth]]
- [[Content Marketing]]
- [[Grain Strategy]]
- [[Board Context]]
- [[Knowledge Graph System]]
- [[Engineering Decisions]]
- [[Voice of the Customer]]

## People
- [[Mike Adams]]
- [[Ryan Owens]]
- [[Jake]]
- [[Ethan]]
- [[Taylor]]
- [[Ben]]

## Companies
(populated by compile)

## Projects
(populated by compile)
```

- [ ] **Step 2: Create topic stubs**

One file per topic in `wiki/topics/`. Each file is just a heading:

`wiki/topics/ICP Validation.md`:
```markdown
# ICP Validation
```

Repeat for: `PLG Growth`, `Content Marketing`, `Grain Strategy`, `Board Context`, `Knowledge Graph System`, `Engineering Decisions`, `Voice of the Customer`.

- [ ] **Step 3: Seed Knowledge Graph System with Mike's quotes**

Replace the stub `wiki/topics/Knowledge Graph System.md` with:

```markdown
# Knowledge Graph System

An LLM-curated wiki as an alternative to vector embeddings for long-term memory. Modeled on [[Andrej Karpathy]]'s concept, built by [[Mike Adams]] across three calls in May 2026.

## Core quotes

> "It's an alternative to like an embeddings model to be able to like perpetually update searchable context." — [[Mike Adams]], May 15

> "The wiki helps to inform the projects inside of that vault. That's the mental model for what goes in cloud code inside of that vault folder. And this is like two weeks old I've been doing this." — [[Mike Adams]], May 15

> "Use the vault when a task needs a lot of context. Use Claude Code for local processing needing libraries or plugins." — [[Mike Adams]]'s heuristic

> "The more bloat you add to the graph, the more potential there is to get things right, but also potential to get things wrong." — [[Mike Adams]], May 14

## Key sessions
- May 6 — 1:1 with Jeff: Introduced the concept, proposed building one
- May 14 — "Automate Your Work with Grain + Claude" webinar: Public demo of vault + compile + wiki
- May 15 — Agentic Workflows internal: Account analysis framework, RAM sales deck output, voice-of-customer vault proposal

## Sources
- Direct observation from three calls (May 6, 14, 15 2026)
```

- [ ] **Step 4: Create people stubs**

One file per person in `wiki/people/`. Each file is just a heading:

`wiki/people/Mike Adams.md`:
```markdown
# Mike Adams

Chairman of [[Grain]]. Built the original Karpathy-style [[Knowledge Graph System]] that this vault is modeled on.
```

For the rest (`Ryan Owens`, `Jake`, `Ethan`, `Taylor`, `Ben`), just the heading:
```markdown
# <Name>
```

- [ ] **Step 5: Create .gitignore**

```
.obsidian/workspace*
.obsidian/cache
.DS_Store
raw/inbox/private/
*.pdf
*.docx
*.pptx
```

- [ ] **Step 6: Initialize git and push**

```bash
cd /Users/Jeff/vault
git init
git add .
git commit -m "Initial vault scaffold"
git remote add origin git@github.com:jeffwhitlock/grain-vault.git
git branch -M main
git push -u origin main
```

- [ ] **Step 7: Verify**

```bash
tree -L 3 /Users/Jeff/vault/
git log --oneline
git remote -v
```

Expected: directory structure matches spec, one commit, remote points to `jeffwhitlock/grain-vault`.

---

## Task 2: Install Obsidian and open the vault

- [ ] **Step 1: Install Obsidian**

```bash
brew install --cask obsidian
```

If already installed, skip.

- [ ] **Step 2: Open the vault in Obsidian**

```bash
open -a Obsidian /Users/Jeff/vault
```

Or: Obsidian → "Open folder as vault" → select `/Users/Jeff/vault/`.

- [ ] **Step 3: Configure Obsidian settings**

In Settings → Core plugins, enable:
- Graph view
- Backlinks
- Outgoing links
- Tag pane

In Settings → Files and links:
- New link format: `Shortest path when possible`
- Use `[[Wikilinks]]`: ON
- Default location for new notes: `wiki/`

- [ ] **Step 4: Verify graph view**

Open graph view (Ctrl/Cmd+G). Confirm nodes appear for the seeded topics and people. Graph will be sparse — that's expected.

- [ ] **Step 5: Commit Obsidian config**

```bash
cd /Users/Jeff/vault
git add .obsidian
git commit -m "Add Obsidian config"
git push
```

---

## Task 3: Create vault CLAUDE.md

**Files:**
- Create: `/Users/Jeff/vault/.claude/CLAUDE.md`

- [ ] **Step 1: Write the CLAUDE.md**

```markdown
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
```

- [ ] **Step 2: Commit**

```bash
cd /Users/Jeff/vault
git add .claude/CLAUDE.md
git commit -m "Add vault CLAUDE.md"
git push
```

- [ ] **Step 3: Verify**

Start a fresh Claude Code session in `/Users/Jeff/vault/` and ask: "What is the pipeline in this vault?" Agent should describe raw → compile → wiki → projects.

---

## Task 4: Create the compile-raw skill

**Files:**
- Create: `/Users/Jeff/vault/.claude/skills/compile-raw/SKILL.md`

- [ ] **Step 1: Write the skill file**

```markdown
---
name: compile-raw
description: Process unprocessed files in raw/ into wiki/ articles. Extract entities, topics, and links. Use whenever Jeff says "compile raw", "update the wiki", "process new meetings", or "run compile".
---

# Compile Raw

You are curating Jeff's personal knowledge graph. Your job is to turn raw inputs into a well-linked wiki.

## Step 1 — Find unprocessed files

Search `raw/meetings/`, `raw/clippings/`, and `raw/inbox/` for markdown files where the frontmatter does NOT contain `processed: true`.

Process oldest first (by frontmatter `date` field, or file mtime if missing).

If there are more than 10 unprocessed files, ask Jeff if he wants to process all or a subset. Token cost scales fast.

## Step 2 — For each raw file

### 2a. Extract entities

Identify:
- **People** mentioned by name (internal Grain team, customers, prospects, public figures)
- **Companies** mentioned
- **Projects / initiatives** referenced
- **Concepts / topics** that are the subject of substantive discussion (not passing mentions)

Be selective. A name mentioned once in passing is not an entity worth a wiki article. A name discussed across multiple inputs is.

### 2b. Extract claims and decisions

For each entity, pull:
- **Direct quotes** where the claim is strong or the language is distinctive
- **Decisions** with date, decider, and rationale
- **Open questions** raised
- **Action items** with owner and (if stated) due date

### 2c. Update or create wiki articles

For each entity:

- **If `wiki/<category>/<entity>.md` exists:** append a new section under a heading like `## Update YYYY-MM-DD from [[Source]]`. Do not modify existing sections.
- **If it does not exist:** create the file. Categories: `topics/`, `people/`, `companies/`, `projects/`.

Every new article must include:
1. A one-sentence definition or summary at the top
2. At least 3 `[[wikilinks]]` to other entities mentioned in the same source
3. A `## Sources` section listing the raw files that contributed

Use Obsidian wikilink syntax `[[Entity Name]]`. The link is what makes the graph view render. **An article with zero outbound links is a failure.**

### 2d. Update wiki/index.md if needed

If a brand-new top-level theme emerged (something that doesn't fit any existing topic), add it to the index under the appropriate section.

### 2e. Mark the raw file processed

Add or update frontmatter:

```yaml
---
processed: true
processed_at: <ISO timestamp>
wiki_articles_touched:
  - topics/Some Topic.md
  - people/Jane Doe.md
---
```

Do NOT delete the raw file. Keep the audit trail.

## Step 3 — Report

After the run, output:

- Files processed: N
- New wiki articles created: list
- Existing wiki articles updated: list
- Any conflicts or ambiguities flagged
- Token usage estimate

## Rules

- **Minimize interpretation.** Lean on direct quotes for strong claims. Paraphrase for context. Flag uncertain interpretations explicitly with `> Uncertain:` blockquote.
- **Cross-link aggressively.** Every meeting mentioning Grain strategy should link to `[[Grain Strategy]]`. Every mention of Mike should link to `[[Mike Adams]]`.
- **Flag, do not merge.** If two existing wiki articles cover overlapping ground, add a `> MERGE CANDIDATE: [[Other Article]]` note. Let Jeff decide.
- **Preserve voice.** Quotes are quotes. Do not paraphrase a quote.
- **Never compress history.** Append-only for updates.

## Anti-patterns to avoid

- Generic recaps. "The team discussed strategy" is useless. Pull the specific point.
- Over-creating people articles. A single passing mention is not enough.
- Re-processing a file. Always check `processed: true` first.
- Silent merges. Flag, don't merge.
```

- [ ] **Step 2: Commit**

```bash
cd /Users/Jeff/vault
git add .claude/skills/compile-raw/SKILL.md
git commit -m "Add compile-raw skill"
git push
```

---

## Task 5: Seed test inputs from Grain MCP and run compile

- [ ] **Step 1: List recent meetings**

Use Grain MCP `list_attended_meetings` for the last 7 days. Pick 3 meetings with distinct topics (e.g., a 1:1, a customer call, an internal review).

- [ ] **Step 2: Fetch and write each meeting**

For each of the 3 meetings, call `fetch_meeting` + `fetch_meeting_transcript`. Write to `raw/meetings/<YYYY-MM-DD>_<slugified-title>.md` with this frontmatter:

```yaml
---
title: <Meeting title>
date: <ISO datetime>
duration: <duration string>
participants: [<names>]
attended: true
processed: false
source: grain
grain_id: <uuid>
grain_url: https://grain.com/recordings/<uuid>
---
```

Body: full transcript markdown from the MCP.

- [ ] **Step 3: Run compile-raw**

Invoke the `compile-raw` skill on the 3 seeded inputs. Observe:
- Were the right entities extracted?
- Are cross-links dense enough?
- Did index.md get updated when warranted?
- Any false merge flags?

- [ ] **Step 4: Check results**

```bash
# All 3 raw files should be marked processed
grep -l "processed: true" /Users/Jeff/vault/raw/meetings/*.md | wc -l
# Expected: 3

# Should have at least 5 new wiki articles
find /Users/Jeff/vault/wiki -name "*.md" -newer /Users/Jeff/vault/wiki/index.md | wc -l

# No empty articles (every .md in wiki/ should contain at least one [[link]])
grep -rL "\[\[" /Users/Jeff/vault/wiki/topics/ /Users/Jeff/vault/wiki/people/ /Users/Jeff/vault/wiki/companies/ /Users/Jeff/vault/wiki/projects/ 2>/dev/null
# Expected: only the initial stubs that haven't been touched yet
```

- [ ] **Step 5: Re-run compile-raw to verify idempotency**

Run compile-raw again. It should report 0 files processed (all marked `processed: true`).

- [ ] **Step 6: Open Obsidian graph view**

Verify clusters and connections from the new articles. Screenshot or confirm visually.

- [ ] **Step 7: Iterate the skill if needed**

If extraction quality is poor, edit `compile-raw/SKILL.md` and re-process one file (temporarily remove `processed: true` from one raw file, run compile, then restore). Expect 3-5 iterations in the first week.

- [ ] **Step 8: Commit**

```bash
cd /Users/Jeff/vault
git add .
git commit -m "Seed 3 Grain meetings and run first compile"
git push
```

---

## Task 6: Build the webhook server

**Files:**
- Create: `server/package.json`
- Create: `server/.env`
- Create: `server/.env.example`
- Create: `server/.gitignore`
- Create: `server/src/index.js`
- Create: `server/src/grain.js`
- Create: `server/src/writer.js`
- Create: `server/src/verify.js`
- Create: `server/README.md`

All paths relative to `/Users/Jeff/Documents/Claude/Projects/Create Knowledge Graph System/server/`.

- [ ] **Step 1: Initialize the project**

```bash
cd /Users/Jeff/Documents/Claude/Projects/Create\ Knowledge\ Graph\ System/server
npm init -y
npm install express dotenv crypto
```

- [ ] **Step 2: Create .gitignore**

```
node_modules/
.env
```

- [ ] **Step 3: Create .env.example**

```
GRAIN_API_KEY=
WEBHOOK_SECRET=
VAULT_PATH=/Users/Jeff/vault
PORT=3000
```

- [ ] **Step 4: Create .env with real values**

```
GRAIN_API_KEY=<the key Jeff provided>
WEBHOOK_SECRET=<generate a random 32-byte hex string>
VAULT_PATH=/Users/Jeff/vault
PORT=3000
```

Generate the webhook secret:
```bash
node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"
```

- [ ] **Step 5: Write src/verify.js**

```javascript
const crypto = require('crypto');

function verifySignature(rawBody, signature, secret) {
  if (!signature || !secret) return false;
  const expected = crypto
    .createHmac('sha256', secret)
    .update(rawBody)
    .digest('hex');
  return crypto.timingSafeEqual(
    Buffer.from(signature),
    Buffer.from(expected)
  );
}

module.exports = { verifySignature };
```

- [ ] **Step 6: Write src/grain.js**

```javascript
const GRAIN_API_BASE = 'https://api.grain.com/_/public-api/v2';

async function fetchRecording(id, apiKey) {
  const res = await fetch(
    `${GRAIN_API_BASE}/recordings/${id}?include=participants,ai_summary,ai_action_items`,
    { headers: { Authorization: `Bearer ${apiKey}` } }
  );
  if (!res.ok) {
    const err = new Error(`Grain API ${res.status}: ${res.statusText}`);
    err.status = res.status;
    throw err;
  }
  return res.json();
}

async function fetchTranscript(id, apiKey) {
  const res = await fetch(
    `${GRAIN_API_BASE}/recordings/${id}/transcript`,
    { headers: { Authorization: `Bearer ${apiKey}` } }
  );
  if (!res.ok) {
    const err = new Error(`Grain transcript API ${res.status}: ${res.statusText}`);
    err.status = res.status;
    throw err;
  }
  return res.json();
}

module.exports = { fetchRecording, fetchTranscript };
```

Note: The exact Grain API base URL and response shapes should be verified against `https://developers.grain.com/` during implementation. The above is based on the docs review. Adjust `fetchTranscript` return type (may be text, not JSON) based on actual API behavior.

- [ ] **Step 7: Write src/writer.js**

```javascript
const fs = require('fs');
const path = require('path');

function slugify(title) {
  return title
    .toLowerCase()
    .replace(/[^a-z0-9]+/g, '-')
    .replace(/-+/g, '-')
    .replace(/^-|-$/g, '')
    .slice(0, 80);
}

function formatDate(isoString) {
  return isoString.slice(0, 10);
}

function buildMarkdown(recording, transcript) {
  const date = formatDate(recording.start_datetime || new Date().toISOString());
  const participants = (recording.participants || [])
    .map(p => p.name || p.email || 'Unknown')
    .filter(Boolean);

  const frontmatter = [
    '---',
    `title: "${(recording.title || 'Untitled').replace(/"/g, '\\"')}"`,
    `date: ${recording.start_datetime || new Date().toISOString()}`,
    `duration: ${recording.duration_ms ? Math.round(recording.duration_ms / 60000) + ' min' : 'unknown'}`,
    `participants: [${participants.map(p => `"${p}"`).join(', ')}]`,
    `attended: true`,
    `processed: false`,
    `source: grain`,
    `grain_id: ${recording.id}`,
    `grain_url: ${recording.url || 'https://grain.com/recordings/' + recording.id}`,
    '---',
  ].join('\n');

  // Format transcript - adapt based on actual API response shape
  let body = '';
  if (Array.isArray(transcript)) {
    body = transcript
      .map(entry => `**${entry.speaker || 'Speaker'}:** ${entry.text || ''}`)
      .join('\n\n');
  } else if (typeof transcript === 'string') {
    body = transcript;
  } else if (transcript && transcript.transcript) {
    body = transcript.transcript;
  }

  return `${frontmatter}\n\n${body}\n`;
}

function writeToVault(recording, transcript, vaultPath) {
  const date = formatDate(recording.start_datetime || new Date().toISOString());
  const slug = slugify(recording.title || 'untitled');
  const filename = `${date}_${slug}.md`;
  const dir = path.join(vaultPath, 'raw', 'meetings');
  const filepath = path.join(dir, filename);

  // Idempotency: check if file with this grain_id already exists
  if (fs.existsSync(dir)) {
    const existing = fs.readdirSync(dir).filter(f => f.endsWith('.md'));
    for (const f of existing) {
      const content = fs.readFileSync(path.join(dir, f), 'utf8');
      if (content.includes(`grain_id: ${recording.id}`)) {
        return { skipped: true, file: f, reason: 'duplicate grain_id' };
      }
    }
  }

  fs.mkdirSync(dir, { recursive: true });
  const markdown = buildMarkdown(recording, transcript);
  fs.writeFileSync(filepath, markdown, 'utf8');
  return { skipped: false, file: filename };
}

module.exports = { writeToVault, slugify, buildMarkdown };
```

- [ ] **Step 8: Write src/index.js**

```javascript
require('dotenv').config();
const express = require('express');
const { verifySignature } = require('./verify');
const { fetchRecording, fetchTranscript } = require('./grain');
const { writeToVault } = require('./writer');

const app = express();
const PORT = process.env.PORT || 3000;
const GRAIN_API_KEY = process.env.GRAIN_API_KEY;
const WEBHOOK_SECRET = process.env.WEBHOOK_SECRET;
const VAULT_PATH = process.env.VAULT_PATH;

// Capture raw body for signature verification
app.use('/webhook/grain', express.json({
  verify: (req, _res, buf) => { req.rawBody = buf.toString(); }
}));
app.use(express.json());

app.get('/health', (_req, res) => {
  res.json({ ok: true, ts: new Date().toISOString() });
});

app.post('/webhook/grain', async (req, res) => {
  // Signature verification (skip if no secret configured — dev mode)
  if (WEBHOOK_SECRET && req.headers['x-grain-signature']) {
    if (!verifySignature(req.rawBody, req.headers['x-grain-signature'], WEBHOOK_SECRET)) {
      console.error('Webhook signature mismatch');
      return res.status(401).json({ error: 'signature mismatch' });
    }
  }

  const payload = req.body;
  const recordingId = payload.data?.id || payload.recording_id;

  if (!recordingId) {
    console.error('No recording ID in payload', JSON.stringify(payload).slice(0, 200));
    return res.status(400).json({ error: 'no recording_id' });
  }

  console.log(`Processing recording: ${recordingId}`);

  try {
    const recording = payload.data || await fetchRecording(recordingId, GRAIN_API_KEY);
    const transcript = await fetchTranscript(recordingId, GRAIN_API_KEY);

    const result = writeToVault(recording, transcript, VAULT_PATH);

    if (result.skipped) {
      console.log(`Skipped (duplicate): ${result.file}`);
      return res.json({ ok: true, skipped: true, file: result.file });
    }

    console.log(`Written: ${result.file}`);
    return res.json({ ok: true, file: result.file });
  } catch (err) {
    console.error(`Error processing ${recordingId}:`, err.message);
    // Auth errors: return 200 so Grain doesn't retry (issue is on our side)
    if (err.status === 401 || err.status === 403) {
      return res.status(200).json({ error: 'auth_failed', grain_id: recordingId });
    }
    // Everything else: return 500 so Grain retries
    return res.status(500).json({ error: err.message, grain_id: recordingId });
  }
});

app.listen(PORT, () => {
  console.log(`Grain webhook server listening on port ${PORT}`);
  console.log(`Vault path: ${VAULT_PATH}`);
});
```

- [ ] **Step 9: Add dev script to package.json**

Add to `package.json` scripts:
```json
{
  "scripts": {
    "start": "node src/index.js",
    "dev": "node --watch src/index.js"
  }
}
```

- [ ] **Step 10: Write server README.md**

```markdown
# Grain Webhook Server

Receives Grain `recording_added` webhooks, fetches the transcript via the Grain workspace API, and writes a markdown file to the vault's `raw/meetings/` folder.

## Setup

```bash
cp .env.example .env
# Fill in GRAIN_API_KEY and WEBHOOK_SECRET
npm install
```

## Run locally

```bash
npm run dev
```

## Expose via ngrok

```bash
ngrok http 3000
```

Copy the https URL and configure in Grain:
- Grain → Settings → API → Webhooks → Add endpoint
- URL: `<ngrok-url>/webhook/grain`
- Event: `recording_added`

## Test

```bash
curl http://localhost:3000/health
```

## Environment variables

| Variable | Description |
|---|---|
| `GRAIN_API_KEY` | Grain workspace API key |
| `WEBHOOK_SECRET` | Shared secret for webhook signature verification |
| `VAULT_PATH` | Absolute path to the vault (default: `/Users/Jeff/vault`) |
| `PORT` | Server port (default: 3000) |
```

- [ ] **Step 11: Test locally**

```bash
cd /Users/Jeff/Documents/Claude/Projects/Create\ Knowledge\ Graph\ System/server
npm run dev &

# Test health endpoint
curl http://localhost:3000/health
# Expected: {"ok":true,"ts":"..."}

# Test with a fake payload using a real grain_id from the seeded meetings
curl -X POST http://localhost:3000/webhook/grain \
  -H "Content-Type: application/json" \
  -d '{"type":"recording_added","data":{"id":"<real-grain-id-from-task-5>","title":"Test Meeting","start_datetime":"2026-05-17T10:00:00Z"}}'
```

Note: The test payload will trigger a real Grain API call to fetch the transcript. Use a `grain_id` from one of the meetings seeded in Task 5.

- [ ] **Step 12: Test idempotency**

Run the same curl command again. Server should return `{"ok":true,"skipped":true,...}` and not create a duplicate file.

- [ ] **Step 13: Commit**

```bash
cd /Users/Jeff/Documents/Claude/Projects/Create\ Knowledge\ Graph\ System/server
git init
git add .
git commit -m "Grain webhook server — local mode"
```

---

## Task 7: Set up ngrok and configure Grain webhook

- [ ] **Step 1: Install ngrok if needed**

```bash
brew install ngrok
```

- [ ] **Step 2: Start the tunnel**

```bash
ngrok http 3000
```

Copy the `https://` forwarding URL (e.g., `https://abc123.ngrok-free.app`).

- [ ] **Step 3: Configure the Grain webhook**

Go to Grain → Settings → API → Webhooks → Add endpoint:
- URL: `<ngrok-url>/webhook/grain`
- Event: `recording_added`
- Secret: the `WEBHOOK_SECRET` value from `.env`

Include parameters (if Grain's UI allows): `participants`, `ai_summary`, `ai_action_items`.

- [ ] **Step 4: Test from Grain**

If Grain's webhook UI has a "Send test" button, use it. Check server logs for the incoming payload. Verify a file appears in `/Users/Jeff/vault/raw/meetings/`.

- [ ] **Step 5: Document the ngrok URL**

Note: ngrok free tier URLs change on restart. For persistence, either:
- Use `ngrok http 3000 --domain=<your-static-domain>` (requires ngrok account)
- Or update the Grain webhook URL each time you restart ngrok

Add a note to the server README about this.

---

## Task 8: End-to-end ingestion test

- [ ] **Step 1: Trigger a real meeting**

Have Jeff start and end a short test Grain meeting (or wait for the next real one).

- [ ] **Step 2: Watch server logs**

Webhook should arrive within 1-5 minutes of recording completion.

```bash
# If running in foreground, logs appear in terminal
# Look for: "Processing recording: <id>" then "Written: <filename>"
```

- [ ] **Step 3: Verify file appeared**

```bash
ls -lt /Users/Jeff/vault/raw/meetings/ | head -5
```

New file should be at the top.

- [ ] **Step 4: Run compile-raw**

Invoke `compile-raw` skill. Verify the new meeting flows into wiki articles correctly.

- [ ] **Step 5: Check wiki in Obsidian**

Open Obsidian graph view. New nodes and connections should appear from the real meeting.

- [ ] **Step 6: Commit**

```bash
cd /Users/Jeff/vault
git add .
git commit -m "First real end-to-end meeting ingestion"
git push
```

---

## Task 9: Create the backfill skill

**Files:**
- Create: `/Users/Jeff/vault/.claude/skills/backfill-grain-meetings/SKILL.md`

- [ ] **Step 1: Write the skill**

```markdown
---
name: backfill-grain-meetings
description: Use the Grain MCP to fetch historical meetings and drop transcripts into raw/meetings/. Skips meetings already present (by grain_id). Use when Jeff says "backfill grain", "pull historical meetings", or after webhook server downtime.
---

# Backfill Grain Meetings

## Step 1 — Determine cutoff
Ask Jeff for a date range, OR default to: from 30 days ago, to now.

## Step 2 — List meetings
Use `list_meetings` (not just `list_attended_meetings`) to include workspace-visible meetings Jeff didn't attend.

## Step 3 — Deduplicate
For each meeting, check `raw/meetings/` for an existing file with the same `grain_id` in frontmatter. Skip duplicates.

## Step 4 — Fetch and write
For each new meeting, use `fetch_meeting` + `fetch_meeting_transcript` and write to `raw/meetings/<YYYY-MM-DD>_<slug>.md` with this frontmatter:

```yaml
---
title: <Meeting title>
date: <ISO datetime>
duration: <duration string>
participants: [<names>]
attended: <true/false>
processed: false
source: grain
grain_id: <uuid>
grain_url: https://grain.com/recordings/<uuid>
---
```

Body: full transcript markdown.

The frontmatter schema MUST match what the webhook server writes. `compile-raw` should not be able to tell webhook-ingested and MCP-ingested files apart.

## Step 5 — Report
Output: count fetched, count skipped (duplicates), any errors.
```

- [ ] **Step 2: Commit**

```bash
cd /Users/Jeff/vault
git add .claude/skills/backfill-grain-meetings/SKILL.md
git commit -m "Add backfill-grain-meetings skill"
git push
```

---

## Task 10: Set up web clipping input

- [ ] **Step 1: Install Obsidian Web Clipper**

Install the Obsidian Web Clipper browser extension from the Chrome Web Store or Firefox Add-ons.

- [ ] **Step 2: Configure the clipper**

Set default destination to: `/Users/Jeff/vault/raw/clippings/`

Configure template frontmatter:
```yaml
---
title: {{title}}
url: {{url}}
date: {{date}}
processed: false
source: web
---
```

- [ ] **Step 3: Test by clipping one article**

Clip any article. Verify the file appears at `/Users/Jeff/vault/raw/clippings/`.

- [ ] **Step 4: Run compile-raw on the clipping**

Invoke compile-raw. Verify it picks up the clipping and produces a useful wiki entry.

- [ ] **Step 5: Commit**

```bash
cd /Users/Jeff/vault
git add .
git commit -m "First web clipping ingested"
git push
```

---

## Task 11: First downstream project

- [ ] **Step 1: Pick a real artifact Jeff owes someone**

Good candidates:
- Weekly Friday company update
- Sales deck for an upcoming customer call
- ICP-validation memo
- Board prep doc

Ask Jeff which one to build.

- [ ] **Step 2: Create the project folder**

```bash
mkdir -p /Users/Jeff/vault/projects/<project-name>
```

- [ ] **Step 3: Write project CLAUDE.md**

```markdown
# Project: <name>

## Goal
<one-sentence outcome>

## Deadline
<date>

## Wiki context to read first
- [[wiki/index.md]]
- [[wiki/topics/<relevant topic>.md]]
(list specific articles)

## Deliverable
<format: pptx? docx? markdown? Slack post?>

## Plan
1. Read listed wiki articles for context
2. Draft the artifact
3. Review with Jeff
```

- [ ] **Step 4: Generate the artifact**

Have the agent produce the deliverable, explicitly reading from the wiki for context. The agent should reference at least 3 distinct wiki articles.

- [ ] **Step 5: Jeff reviews**

Jeff confirms the output is at least as good as his usual baseline. If not, iterate the compile skill and try again.

- [ ] **Step 6: Commit**

```bash
cd /Users/Jeff/vault
git add .
git commit -m "First downstream project: <name>"
git push
```

---

## Task 12: Create the daily-brief skill

**Files:**
- Create: `/Users/Jeff/vault/.claude/skills/daily-brief/SKILL.md`

- [ ] **Step 1: Write the skill**

```markdown
---
name: daily-brief
description: Produce Jeff's morning briefing. Reads today's calendar, recent wiki updates, open projects. Use when Jeff says "daily brief", "morning brief", or "what's on my plate".
---

# Daily Brief

## Step 1 — Calendar
Pull today's calendar events via Google Calendar MCP. For each:
- Title, time, attendees
- For external meetings: search wiki/companies/ and wiki/people/ for matching articles. Include a one-line summary of what we know about them.

## Step 2 — Recent wiki updates
List wiki articles modified in the last 24 hours (use file mtime). Summarize what changed in each.

## Step 3 — Open projects
For each subfolder in projects/, read the CLAUDE.md and report: name, deadline, next step.

## Step 4 — Format

Output as a structured brief:

```
# Daily Brief — <date>

## Today's calendar
- HH:MM — <Event> with <attendees>
  - Context: [[wiki article]] — one-line summary

## Wiki changes (last 24h)
- [[Article]] — what changed

## Open projects
- <name> (deadline: <date>) — next step: <action>

## Suggested priority
<one-line: what should Jeff do first based on the above>
```
```

- [ ] **Step 2: Test the skill**

Invoke `daily-brief`. Verify it pulls real calendar events and references real wiki articles.

- [ ] **Step 3: Commit**

```bash
cd /Users/Jeff/vault
git add .claude/skills/daily-brief/SKILL.md
git commit -m "Add daily-brief skill"
git push
```

---

## Task 13: Documentation and final commit

**Files:**
- Create: `/Users/Jeff/vault/README.md`
- Create: `/Users/Jeff/vault/decisions/`

- [ ] **Step 1: Write README.md**

```markdown
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

## Open questions

- Cloud-hosted vault so it runs without laptop on?
- Team-level voice-of-customer vault (Mike to propose)
- Cost monitoring on compile runs
- ngrok static domain for persistent webhook URL

## When to retire this

Mike said he might throw his out in 2-3 months. Same posture here. If after 6 weeks the outputs aren't noticeably better than baseline, kill it and write a postmortem.
```

- [ ] **Step 2: Create decisions directory**

```bash
mkdir -p /Users/Jeff/vault/decisions
```

- [ ] **Step 3: Final commit**

```bash
cd /Users/Jeff/vault
git add .
git commit -m "Documentation and README"
git push
```

- [ ] **Step 4: Final verification checklist**

- [ ] Vault exists at `/Users/Jeff/vault/` with full directory structure
- [ ] `compile-raw` skill processes at least 3 seeded test inputs into wiki articles with backlinks
- [ ] Grain meeting ingestion works end-to-end (webhook → file → compile → wiki)
- [ ] At least one real downstream artifact generated by a project that read from the wiki
- [ ] Git repo initialized, pushed to `jeffwhitlock/grain-vault`
- [ ] README.md at vault root explains the system

---

## Dependency graph

```
Task 1 (scaffold + git)
  → Task 2 (Obsidian) [parallel-safe with Task 3]
  → Task 3 (CLAUDE.md) [parallel-safe with Task 2]
    → Task 4 (compile-raw skill)
      → Task 5 (seed + run compile) — needs Grain MCP
        → Task 6 (webhook server)
          → Task 7 (ngrok + Grain config)
            → Task 8 (end-to-end test)
        → Task 9 (backfill skill) [parallel-safe with Task 6]
        → Task 10 (web clipper) [parallel-safe with Task 6]
      → Task 11 (downstream project) — needs wiki populated
        → Task 12 (daily-brief) [parallel-safe with Task 11]
          → Task 13 (docs + final commit)
```

Tasks 2+3 can run in parallel. Tasks 6, 9, 10 can run in parallel after Task 5. Tasks 11 and 12 can run in parallel.
