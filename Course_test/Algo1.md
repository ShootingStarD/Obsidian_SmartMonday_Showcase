---
short_name: Algo1
year: BA1
mnemonic: 
tags:
  - course
  - "#algo"
---

# Course Notes 
```dataview
Table session_title, session_number, to_rework, data, concepts_seen
from #course_session 
where course = this.short_name
```

# Questions

```dataview
task
from #course_session
where course = this.short_name and contains(tags, "#question")
```

# Modalités Evaluations

```dataview
list without id
L.text
from #course_session
flatten file.lists as L
where course = this.short_name and contains(L.tags, "#modalité-évaluation")
```
