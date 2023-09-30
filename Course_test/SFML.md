---
short_name: SFML
year: MA1
mnemonic: INFO-F422
tags:
  - course
  - machine-learning
  - R
cssclasses:
  - cards
  - table-wide
  - list-cards
---

# Course Notes 
```dataview
table session_title, session_number, to_rework, date, concepts_seen, progress
from #course_session 
where course = this.file.link
```
# Remaining questions

```dataview
TABLE WITHOUT ID file.link as "Session", C.text as "Remaining questions" 
FROM #course_session and #Questions
FLATTEN file.lists as L 
WHERE course = this.file.link and  join(L.tags, "") = "#Questions" 
FLATTEN L.children as C
```


# Modalités Evaluations
```dataview
list without id
L.text
from #course_session
flatten file.lists as L
where course = this.file.link and contains(L.tags, "#modalité-évaluation")
```