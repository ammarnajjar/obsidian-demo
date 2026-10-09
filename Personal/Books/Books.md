---
tags:
  - navigation
---
# Reading dashboard
## Currently reading
```dataview
TABLE author AS "Author", created AS "Added"
FROM #book
WHERE status = "reading"
SORT created DESC
```
## Recently added
```dataview
TABLE author AS "Author", created AS "Added", status AS "Status"
FROM #book
SORT created DESC
LIMIT 5
```
## Top rated
```dataview
TABLE author AS "Author", rating AS "Rating"
FROM #book
WHERE rating >= 4
SORT rating DESC
```
## Unrated
```dataview
TABLE author AS "Author", status AS "Status"
FROM #book
WHERE rating = null
SORT created DESC
```
## By status
```dataview
TABLE rows.file.link AS "Books", length(rows) AS "Count"
FROM #book
GROUP BY status
```
