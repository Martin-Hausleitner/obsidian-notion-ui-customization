---
database-plugin: basic
type: "database-view"
status: "active"
emoji: "🗃️"
tags:
  - demo
  - database
  - dbfolder
---

# 🗃️ Company Demo DB

```yaml:dbfolder
name: Company Demo
description: Kompakte DB-Folder-Ansicht fuer die Demo-Seiten.
columns:
  __file__:
    key: __file__
    accessorKey: __file__
    input: markdown
    label: Page
    accessor: __file__
    isMetadata: true
    position: 1
    config:
  status:
    input: select
    accessor: status
    label: Status
    key: status
    accessorKey: status
    position: 2
    options:
      - { label: "automated", backgroundColor: "hsl(154, 35%, 88%)" }
      - { label: "live", backgroundColor: "hsl(203, 38%, 88%)" }
      - { label: "planned", backgroundColor: "hsl(43, 42%, 88%)" }
    config:
      isInline: false
  owner:
    input: text
    accessor: owner
    label: Owner
    key: owner
    accessorKey: owner
    position: 3
    config:
      isInline: false
  sync:
    input: text
    accessor: sync
    label: Sync
    key: sync
    accessorKey: sync
    position: 4
    config:
      isInline: false
  priority:
    input: number
    accessor: priority
    label: Priority
    key: priority
    accessorKey: priority
    position: 5
    isSorted: true
    isSortedDesc: true
    config:
      isInline: false
config:
  enable_show_state: false
  group_folder_column: none
  cell_size: normal
  sticky_first_column: false
  remove_field_when_delete_column: false
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: dataview
  source_form_result: FROM "05_Demo" WHERE type = "company-demo"
  source_destination_path: /
  row_templates_folder: /
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  pagination_size: 10
  font_size: 16
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: false
  last_field: false
  date_format: yyyy-MM-dd
  datetime_format: yyyy-MM-dd HH:mm:ss
  metadata_date_format: yyyy-MM-dd
  metadata_datetime_format: yyyy-MM-dd HH:mm:ss
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions: []
```
