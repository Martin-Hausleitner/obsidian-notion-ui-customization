---
type: "dashboard"
status: "active"
emoji: "📊"
banner: "![[99_Assets/notion-dashboard-banner.png]]"
banner_y: 0.42
banner_icon: "📊"
tags:
  - dashboard
  - database
  - dataview
  - sqlseal
---

# 📊 Data Tables

<div class="notion-company-kicker">Fuenf ruhige Varianten fuer professionelle Datenansichten: Markdown-Tabelle, Bases, DB Folder, Dataview und SQLSeal.</div>

## Kompakt

| Page | Status | Owner | Sync |
| --- | --- | --- | --- |
| 🐙 GitHub Backup | automated | Operations | Obsidian Git |
| 📚 Knowledge Base | live | Team | Markdown |
| 🧭 Customer Portal | planned | Product | Notion-ready |

<details class="notion-more">
<summary>Mehr anzeigen</summary>

- **Bases** ist am besten fuer Obsidian-native Datenbank-Views ueber lokale Markdown-Properties.
- **DB Folder** ist am besten fuer eine Notion-aehnliche Datenbank-Datei mit editierbaren Spalten.
- **Dataview** ist am besten fuer schnelle Property-Abfragen aus Markdown-Seiten.
- **SQLSeal** ist am besten fuer SQL, CSV, globale Tabellen und analysierbare Daten.

</details>

## Bases

![[Company Demo.base]]

## DB Folder

![[Company Demo DB]]

## Dataview

```dataview
TABLE status AS "Status", owner AS "Owner", sync AS "Sync", priority AS "Priority"
FROM "05_Demo"
WHERE type = "company-demo"
SORT priority DESC
```

## SQLSeal

```sqlseal
TABLE company_sync = file(99_Assets/data/company_sync.csv)

SELECT area, status, owner, sync
FROM company_sync
ORDER BY priority DESC
LIMIT 10
```
