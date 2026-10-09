# Master Task List

Pinned demo note. Open tasks from daily and work notes, grouped by source note.

```dataview
TASK
WHERE !completed AND (startswith(file.path, "Daily/") OR startswith(file.path, "Work/"))
SORT file.mtime DESC
GROUP BY file.link
```
