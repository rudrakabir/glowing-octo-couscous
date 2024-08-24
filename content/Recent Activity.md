# Recent Activity

## Recently Edited Files

```dataview
TABLE WITHOUT ID
file.link AS "Note", dateformat(file.mtime, "yyyy-MM-dd") AS "Last Modified"
SORT file.mtime DESC
LIMIT 7
```


## Recently Created
```dataview
TABLE WITHOUT ID
file.link AS "Note", dateformat(file.ctime, "yyyy-MM-dd") AS "Created"
SORT file.ctime DESC
LIMIT 7
```
