---
number:
start-date:
end-date:
tags:
  - semester
---
# [[<% tp.file.title %>]]
## Courses
```dataview
TABLE without ID
	file.link AS "Course",
	course-title AS "Course Title",
	credits AS "Credits",
	grade AS "Grade"
FROM #course 
WHERE semester = this.file.link
SORT file.name ASC
```