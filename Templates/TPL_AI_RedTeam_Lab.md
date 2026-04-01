---
date: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - red-team
  - ai-security
  - lab
status: In Progress
target_system:
owasp_category:
severity:
tool_used:
trackobsidian://open?vault=Bentley&file=vault%2FTemplates%2FTPL_AI_RedTeam_Lab: technical
---

# 🔴 AI Red Team Lab — <% tp.date.now("YYYY-MM-DD") %> — `{{target_system}}`

---

## 📋 Test Metadata

| Field | Value |
|-------|-------|
| **Target System / Agent** | |
| **Test Environment** | ☐ Sandbox  ☐ Staging  ☐ Prod (read-only) |
| **Tool Used** | ☐ PyRIT  ☐ Garak  ☐ Manual  ☐ Other: |
| **OWASP LLM Category** | |
| **OWASP Agentic Category** | |
| **Severity (if confirmed)** | ☐ Critical  ☐ High  ☐ Medium  ☐ Low  ☐ Info |
| **Time Spent** | |

---

## 🎯 Objective

> What behavior are you trying to elicit or break? Be specific about the threat model.


**Threat actor assumption:**
> (e.g., Insider threat, external user with API access, compromised tool endpoint)

---

## 📥 Initial Prompt / Input

> Paste the exact prompt, input, or instruction used to begin the test.

```
[PROMPT START]

[PROMPT END]
```

**Context injected (system prompt, tool output, RAG chunk, etc.):**
```
[CONTEXT START]

[CONTEXT END]
```

---

## ⚔️ Attack Vector

> Describe the vector and which OWASP category it maps to.

**Vector type:**
☐ Prompt Injection (LLM01)
☐ Sensitive Data Exposure (LLM02)
☐ Supply Chain (LLM03)
☐ Data / Model Poisoning (LLM04)
☐ Improper Output Handling (LLM05)
☐ Excessive Agency (LLM06)
☐ System Prompt Leakage (LLM07)
☐ Vector / Embedding Weakness (LLM08)
☐ Misinformation (LLM09)
☐ Unbounded Consumption (LLM10)
☐ Agent Goal Hijacking (Agentic-01)
☐ Tool Misuse / Abuse (Agentic-02)
☐ Memory Poisoning (Agentic-03)
☐ Other: ___

**Narrative description of vector:**


---

## 🔓 Bypass Method

> How did you get past guardrails (if at all)? Be precise — this is the most valuable part of the log.

**Technique used:**


**Iterations attempted before success:**

| Attempt | Prompt Variation | Result |
|---------|-----------------|--------|
| 1 | | |
| 2 | | |
| 3 | | |

**Successful payload (if applicable):**
```
[PAYLOAD]

[/PAYLOAD]
```

---

## 📊 Model / System Response

> Paste or summarize the actual output that confirmed the finding.

```
[RESPONSE START]

[RESPONSE END]
```

**Why this response is a problem:**


---

## 🛡️ Remediation Recommendation

> Write this as if it's going into a findings report. Clear, actionable, non-technical where possible.

**Short-form (for exec summary):**


**Technical recommendation:**


**Priority:** ☐ Immediate  ☐ Next Sprint  ☐ Backlog

**Suggested owner:** ☐ ML/AI Team  ☐ AppSec  ☐ Platform  ☐ Policy

---

## 📣 Comms Translation

> Draft how you'd explain this finding to a non-technical employee or business stakeholder.


---

## 🔗 References & Related

- OWASP LLM Top 10: https://owasp.org/www-project-top-10-for-large-language-model-applications/
- OWASP Agentic: https://owasp.org/www-project-top-10-for-agentic-ai/
- Related lab: [[]]
- Related project: [[]]

---

## ✅ Status

☐ Finding confirmed
☐ Finding disputed / needs retest
☐ False positive
☐ Reported to team
☐ Remediation verified
