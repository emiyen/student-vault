# [[Home]]
## Semesters
```base
filters:
  and:
    - file.tags.contains("semester")
    - file.folder != "00 SYSTEM/templates"
views:
  - type: table
    name: Table
    order:
      - file.name
      - start-date
      - end-date
    sort:
      - property: number
        direction: ASC
    columnSize:
      file.name: 460
      note.start-date: 122

```

## Course Overview
```base
filters:
  and:
    - file.tags.contains("course")
    - file.folder != "00 SYSTEM/templates"
views:
  - type: table
    name: Table
    groupBy:
      property: semester
      direction: ASC
    order:
      - file.name
      - credits
      - grade
    columnSize:
      file.name: 460
      note.credits: 121

```
