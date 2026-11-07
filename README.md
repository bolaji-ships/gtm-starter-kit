# GTM Starter Kit

Claude Code skills, playbooks and tools for building go-to-market systems. Copy them into your own Context OS and Claude Code can use them straight away.

## How to use it

Open Claude Code in your Context OS folder and paste:

> Clone github.com/bolaji-ships/gtm-starter-kit into a temporary folder. Copy its .claude/skills folders into our .claude/skills, its knowledge-base/playbooks folder into our knowledge-base/playbooks, and its tools folder into our tools. Don't overwrite our own files. Delete the temporary folder, then list what you added.

Start a new Claude Code session afterwards so the skills load. Type `/` to see them.

## Skills

**From research to copy.** Run them in this order:

| Skill | What it does |
|---|---|
| `campaign-strategy` | 15 to 25 outbound campaign ideas from your website and ICP, each tagged with its mother intent and a Tier 1 to 3 priority |
| `signal-matrix` | ICP segments, the buying signals that find them, and the 3 to 5 signals to build first |
| `build-workflow-spec` | The structure of one workflow: mother intent, sources, signals with their roles, a routing matrix with an angle per cell, and the variables copy may use. Writes no copy |
| `campaign-copy` | Turns an approved workflow spec into cold email and LinkedIn copy, one email at a time, from verified facts only |
| `miro-gtm-flowchart` | Draws your GTM system as an editable flow chart on a Miro board |

**Building in Clay** (uses `tools/rex`):

| Skill | What it does |
|---|---|
| `build-clay` | Build or audit an outbound workbook: Companies table, people sourcing, one shared People table |
| `prompt-builder` | Per-row prompts for AI columns, with JSON output, tested on the model that runs them |
| `campaign-contract`, `design-clay-table-json`, `import-clay-table`, `save-clay-schema` | Contract-first table builds: plan, design, import with a one-row proof and a budget check, then save the approved schema |
| `calculate-costs`, `workspace-cost-audit` | What a table, or a whole workspace in a month, actually cost |
| `export-tables` | Export Clay tables to CSV |
| `campaign-qa` | QA a Clay table or sequencer campaign against its workflow spec before launch |

**Research and deliverability:**

| Skill | What it does |
|---|---|
| `crawl4ai` | Crawl pages or whole sites into Markdown, free and local |
| `agent-browser` | Drive a real browser: click, fill forms, log in, screenshot |
| `inbox-placement-test` | Test where your cold emails land (inbox, promotions or spam) across your sending mailboxes. Built for EmailBison and MailReach |

## Playbooks

`knowledge-base/playbooks/` holds the method docs the skills read:

- `workflow-anatomy.md`: the Mother Intent Catalog and the structure of a signal-based workflow
- `signal-matrix-framework.md`: how to segment an ICP and validate signals
- `copy-iron-laws.md`, `copy-frameworks.md`, `linkedin-dm-frameworks.md`, `copy-bans.yaml`: the rules and patterns behind the copy
- `templates/facts-template.md`: the facts file `campaign-copy` needs (approved proof, claims, banned words, sender)
- `clay/`: what costs Clay credits, a Clay expert guide, AI column prompts, formulas and Clay rules

## Tools

- `tools/rex/`: an unofficial Python SDK that lets Claude Code work inside Clay with your own browser session. Not affiliated with Clay. Start with `tools/rex/GETTING_STARTED.md`.
- `tools/crawl4ai/` and `tools/agent-browser/`: install guides. Both tools are open source and installed separately.

## Folder layout

The repo is laid out as a Context OS: one folder that holds everything Claude Code needs to know about your go-to-market.

```
.claude/skills/        Claude Code skills, one folder each with a SKILL.md
context/
  icp/                 ICP, personas, signal matrix
  positioning/         positioning, value proposition, competitors
  messaging/           core message, pillars, facts.md
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

Empty folders hold a `.gitkeep` file so Git keeps them. `.env`, Clay session files and lead lists are in `.gitignore` and never get committed. If you put real workspace ids, customer names or campaign data in your own copy, keep that repo private.

## Credits

Some parts are adapted from other open-source projects. See [THIRD-PARTY.md](THIRD-PARTY.md).
