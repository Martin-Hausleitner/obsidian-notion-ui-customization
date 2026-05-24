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

<div class="notion-company-kicker">Drei Varianten fuer professionelle Datenansichten: einfache Tabelle, Dataview und SQLSeal.</div>

## Kompakt

<div class="notion-table-card">
<table>
  <thead>
    <tr>
      <th>Page</th>
      <th>Status</th>
      <th>Owner</th>
      <th>Sync</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>🐙 GitHub Backup</td>
      <td>automated</td>
      <td>Operations</td>
      <td>Obsidian Git</td>
    </tr>
    <tr>
      <td>📚 Knowledge Base</td>
      <td>live</td>
      <td>Team</td>
      <td>Markdown</td>
    </tr>
    <tr>
      <td>🧭 Customer Portal</td>
      <td>planned</td>
      <td>Product</td>
      <td>Notion-ready</td>
    </tr>
  </tbody>
</table>
</div>

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
