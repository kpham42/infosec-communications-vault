# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

This is the Obsidian vault configuration and template set for Kevin Pham's Bentley Systems InfoSec internship (Summer/Fall 2026). The working directory (`.obsidian/`) contains Obsidian app config and template `.md` files. The actual vault content lives in `../vault/`.

## Vault Structure

```
../vault/
├── 00_Daily/          ← Daily notes (TPL_Daily_Note)
├── 01_Projects/       ← Technical/ and Comms/ subfolders, queried by Project Dashboard
├── 02_Learning/       ← HTB/, Python/, Courses/
├── 03_Security_Policy/
├── 04_Red_Teaming/    ← Tests/, Findings/, Methodology/
├── 05_Agentic_AI_Governance/  ← Priority track; Threat_Models/, Labs/, Policy_Drafts/
├── 06_ICS_SCADA/
├── 07_Meetings/
├── 08_References/
└── Templates/         ← Copies of the .obsidian template files
```

## Required Plugins

Community plugins (configured in `community-plugins.json`):
- **Templater** (`templater-obsidian`) — processes `<% %>` dynamic fields in templates
- **Dataview** — powers SQL-like queries in `TPL_Project_Dashboard.md`
- **Calendar** — daily note navigation
- **Git** (`obsidian-git`) — vault version control

## Templates

All templates live in both `.obsidian/` and `../vault/Templates/`. They use Templater syntax (`<% tp.date.now(...) %>`) for dynamic date fields and `{{placeholder}}` markers for manual fill-in.

| File | Purpose |
|------|---------|
| `TPL_Daily_Note.md` | Daily work log with technical wins, comms tasks, AI red team activity, Python snippet |
| `TPL_AI_RedTeam_Lab.md` | Structured finding log — maps to OWASP LLM Top 10 and Agentic AI Top 10 |
| `TPL_HTB_Lab.md` | HTB machine/challenge notes with recon, exploitation, flags sections |
| `TPL_Meeting_Note.md` | Meeting notes with mandatory "Translation" section for non-technical stakeholders |
| `TPL_Project_Note.md` | Project tracking note; `track` field (`technical`/`comms`) feeds Dataview dashboard |
| `TPL_Project_Dashboard.md` | Pinned Dataview dashboard — queries `01_Projects/`, `04_Red_Teaming/Tests/`, `02_Learning/HTB/` |

## Frontmatter Conventions

Notes that feed Dataview queries must include these fields accurately:

- `track`: `technical` or `comms` (used by Project Dashboard)
- `status`: free text but dashboard displays it literally — use the status key symbols (🟢/🔄/🔴/⏸️/📋)
- `priority`: integer (1 = highest)
- `owasp_category`, `severity`, `target_system`: used by AI Red Team log query
- `htb_track`, `difficulty`, `completed`: used by HTB progress query

## Doc-as-Code Workflow

```bash
# Daily commit habit from vault root (../vault/)
git add .
git commit -m "daily: YYYY-MM-DD"
git push
```

The Obsidian Git plugin can automate this on a timer.

## Key Focus Areas

`05_Agentic_AI_Governance/` is the priority track for the internship. Focus areas:
- **Agentic-01** Agent Goal Hijacking
- **Agentic-02** Tool Misuse / Abuse
- **Agentic-03** Memory Poisoning
- Privilege escalation through chained tool calls in digital twin / ICS environments

Testing tools: PyRIT (Microsoft), Garak. Reference frameworks: OWASP LLM Top 10, OWASP Agentic AI Top 10, NIST AI RMF.
