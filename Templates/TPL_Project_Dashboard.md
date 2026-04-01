---
date: <% tp.date.now("YYYY-MM-DD") %>
tags: [dashboard, tracker]
---

# 📊 Internship Project Tracker — Bentley Systems Fall 2026

> **Kevin Pham** | InfoSec Intern | Updated: <% tp.date.now("MMMM YYYY") %>

---

## 🔧 Track 1 — Technical & Research

```dataview
TABLE
  status AS "Status",
  priority AS "Priority",
  due AS "Due",
  file.link AS "Project"
FROM "01_Projects"
WHERE track = "technical"
SORT priority ASC
```

---

## 📣 Track 2 — Comms & Policy

```dataview
TABLE
  status AS "Status",
  priority AS "Priority",
  due AS "Due",
  file.link AS "Project"
FROM "01_Projects"
WHERE track = "comms"
SORT priority ASC
```

---

## 🤖 AI Red Team Log

```dataview
TABLE
  target_system AS "Target",
  owasp_category AS "OWASP",
  severity AS "Severity",
  status AS "Status"
FROM "04_Red_Teaming/Tests"
SORT date DESC
```

---

## 🎮 HTB Progress

```dataview
TABLE
  htb_track AS "Track",
  difficulty AS "Difficulty",
  status AS "Status",
  completed AS "Completed"
FROM "02_Learning/HTB"
SORT completed DESC
```

---

## 📅 Recent Daily Notes

```dataview
LIST
FROM "00_Daily"
SORT date DESC
LIMIT 7
```

---

## 📈 Weekly Snapshot

> Fill this in manually each Friday.

| Week | Technical Win | Comms Win | Python Reps | HTB Progress |
|------|--------------|-----------|-------------|--------------|
| W1 | | | | |
| W2 | | | | |
| W3 | | | | |
| W4 | | | | |
| W5 | | | | |
| W6 | | | | |
| W7 | | | | |
| W8 | | | | |
| W9 | | | | |
| W10 | | | | |
| W11 | | | | |
| W12 | | | | |

---

## 🏷️ Status Key

| Symbol | Meaning |
|--------|---------|
| 🟢 | Complete |
| 🔄 | In Progress |
| 🔴 | Blocked |
| ⏸️ | On Hold |
| 📋 | Not Started |
