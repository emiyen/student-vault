---
semester:
course-title:
credits:
grade:
tags:
  - course
---
# [[<% tp.file.title %>]]
## Lecture Notes
```base
filters:
  or:
    - file.hasTag("notes/lecture")
views:
  - type: table
    name: Table
    filters:
      and:
        - course == link("<% tp.file.title %>")
    order:
      - file.name
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 518

```

## Textbook Notes
```base
filters:
  or:
    - file.hasTag("notes/textbook")
views:
  - type: table
    name: Table
    filters:
      and:
        - course == link("<% tp.file.title %>")
    order:
      - file.name
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 518

```