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
