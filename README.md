# Kevin Pham — Security Communications Internship Vault and Knowledge
## Summer 2026

---

## Vault Purpose

This vault is a living knowledge base for an information security communications internship this upcoming summer and fall. It tracks my technical growth, red teaming work, policy communications, and learning as an aspiring technical communications engineer and AI safety professional.

Of course, this is just a public template with placeholder whitespace. No sensitive information about my employer can be found here. This basic structure is for demostrative purposes only. 

---

## Folder Structure

```
📁 Vault Root
│
├── 📁 00_Daily/
│     └── YYYY-MM-DD.md          ← Daily notes (use TPL_Daily_Note)
│
├── 📁 01_Projects/
│     ├── Technical/              ← track: technical
│     └── Comms/                  ← track: comms
│
├── 📁 02_Learning/
│     ├── HTB/                    ← HTB lab notes (use TPL_HTB_Lab)
│     │     ├── AI_Red_Teamer/
│     │     └── ICS_Track/
│     ├── Python/                 ← Scripts, snippets, mini-projects
│     └── Courses/                ← SANS, certifications, reading notes
│
├── 📁 03_Security_Policy/
│     ├── Awareness_Campaigns/    ← Internal comms drafts
│     ├── Policy_Docs/            ← Policy rewrites and guides
│     └── Communications/         ← Finished deliverables
│
├── 📁 04_Red_Teaming/
│     ├── Tests/                  ← Lab notes (use TPL_AI_RedTeam_Lab)
│     ├── Findings/               ← Confirmed findings and reports
│     └── Methodology/            ← Reference notes: OWASP, PyRIT, Garak
│
├── 📁 05_Agentic_AI_Governance/  ← ⭐ Priority track (see note below)
│     ├── Threat_Models/          ← Agent-specific threat modeling
│     ├── Labs/                   ← Agentic red team tests
│     └── Policy_Drafts/          ← Internal AI governance docs
│
├── 📁 06_ICS_SCADA/
│     ├── Protocols/              ← Modbus, DNP3 notes
│     ├── Digital_Twins/          ← Bentley-specific context
│     └── Resources/
│
├── 📁 07_Meetings/
│     └── YYYY-MM-DD_Topic.md     ← Meeting notes (use TPL_Meeting_Note)
│
├── 📁 08_References/
│     ├── OWASP/
│     ├── NIST/
│     └── Frameworks/
│
└── 📁 Templates/
      ├── TPL_Daily_Note.md
      ├── TPL_AI_RedTeam_Lab.md
      ├── TPL_HTB_Lab.md
      ├── TPL_Meeting_Note.md
      ├── TPL_Project_Note.md
      └── TPL_Project_Dashboard.md
```

---

## Templates Quick Reference

| Template | Use When |
|----------|----------|
| `TPL_Daily_Note` | Every workday — morning setup |
| `TPL_AI_RedTeam_Lab` | Starting any adversarial test session |
| `TPL_HTB_Lab` | Beginning a new HTB machine or challenge |
| `TPL_Meeting_Note` | Any meeting — fill Translation section always |
| `TPL_Project_Note` | Starting a new project or initiative |
| `TPL_Project_Dashboard` | Pin this to your sidebar — update weekly |

---

## Required Plugins

Install these from Obsidian Community Plugins:

- **Dataview** — Powers the dashboard queries
- **Templater** — Powers the `<% %>` dynamic fields in templates
- **Calendar** — Daily note navigation
- **Git** — For doc-as-code version control of the vault

---

## Agentic AI Governance — Priority Focus

Internal AI agents that take actions in infrastructure software (not just answer questions) represent an entirely different threat surface than standard LLM deployments.

**The folder `05_Agentic_AI_Governance/` exists specifically for this.**

Key focus areas:
- Agent Goal Hijacking (OWASP Agentic-01): Can an adversarial input redirect an agent's objective mid-task?
- Tool Misuse (Agentic-02): Can an agent be coerced into abusing a connected tool or API?
- Memory Poisoning (Agentic-03): Can persistent agent memory be corrupted to change future behavior?
- Privilege escalation through chained tool calls in digital twin environments

Red teaming agentic systems at a company like Bentley — where AI agents may eventually interface with infrastructure data — is legitimately advanced work. Document everything.

---

## Doc-as-Code Workflow

```bash
# Initialize git in vault root
git init
git remote add origin <your-private-repo>

# Daily commit habit
git add .
git commit -m "daily: YYYY-MM-DD"
git push
```

Use the Obsidian Git plugin to automate this on a timer if preferred.

---

## Key External Resources

| Resource | URL |
|----------|-----|
| OWASP LLM Top 10 | https://owasp.org/www-project-top-10-for-large-language-model-applications/ |
| OWASP Agentic AI Top 10 | https://owasp.org/www-project-top-10-for-agentic-ai/ |
| PyRIT (Microsoft) | https://github.com/Azure/PyRIT |
| Garak | https://github.com/leondz/garak |
| SANS SIFT | https://www.sans.org/tools/sift-workstation/ |
| HTB AI Red Teamer Path | https://app.hackthebox.com/tracks |
| NIST AI RMF | https://airc.nist.gov/RMF |

---

*Vault initialized: <% tp.date.now("MMMM YYYY") %>*
