---
tags:
  - technical
area: Architecture
---
# Dataview patterns used here
Person pages use `LIST FROM [[Person]] SORT file.mtime DESC`.
The reading dashboard uses `TABLE author AS "Author", created AS "Added" FROM #book WHERE status = "reading"`.
