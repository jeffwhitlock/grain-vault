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
