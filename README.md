# GTM Starter Kit

Claude Code skills and playbooks for building go-to-market systems. Copy them into your own Context OS and Claude Code can use them straight away.

## What's inside

The repo is laid out as a Context OS: one folder that holds everything Claude Code needs to know about your go-to-market.

```
.claude/skills/        Claude Code skills, one folder each with a SKILL.md
context/
  icp/                 ICP, personas, signal matrix
  positioning/         positioning, value proposition, competitors
  messaging/           core message, pillars, angles per persona
  brand-kit/           tone of voice, key phrases, logos
  docs/                research, case studies, GTM system map
knowledge-base/
  playbooks/           method docs the skills read
  learnings/           what worked and what didn't
meetings/              call notes, one file per meeting
output/campaigns/      campaign strategy, one folder per workflow
tools/                 scripts and tools, each with its own README
weekly-priorities/     one file per week, linked to that week's work log
work-log/              one file per week, every change timestamped
```

Empty folders hold a `.gitkeep` file so Git keeps them. `.env` (your API keys) is in `.gitignore` and never gets committed.

## How to use it

Open Claude Code in your Context OS folder and paste:

> Clone github.com/bolaji-ships/gtm-starter-kit into a temporary folder. Copy its .claude/skills folders into our .claude/skills and its knowledge-base/playbooks files into our knowledge-base/playbooks. Delete the temporary folder, then list what you added.

Start a new Claude Code session afterwards so the skills load.
