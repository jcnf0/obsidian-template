# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>
<< [[<% moment(tp.file.title,'YYYY-MM-DD_ddd').subtract(1, 'days').format("YYYY-MM-DD_ddd") %>|Yesterday]] | [[<% moment(tp.file.title,'YYYY-MM-DD_ddd').add(1, 'days').format("YYYY-MM-DD_ddd") %>|Tomorrow]] >>

---
# Weekly Note : [[{{date:gggg-[W]ww}}]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[review]` `BUTTON[thought]`

---
# Notes


---
# Tasks
```tasks
scheduled {{date:YYYY-MM-DD}}
limit 20
sort by priority
sort by due date
group by function task.tags.map( (tag) => tag.split('/')[1] ? tag.split('/').slice(1, 2) : '').filter( (tag) => tag.includes("SHALLOW") | tag.includes("DEEP") )
hide tags
hide due date
```
---
# Notes Created Today
```dataview
LIST FROM "CLASSES" OR "PERSONAL" OR "RESEARCH" WHERE file.cday = date("<%moment(tp.file.title,'YYYY-MM-DD').format('YYYY-MM-DD')%>") SORT file.ctime asc
LIMIT 5
```

# Notes Edited Today
```dataview
LIST FROM "CLASSES" OR "PERSONAL" OR "RESEARCH" WHERE file.mday = date("<%moment(tp.file.title,'YYYY-MM-DD').format('YYYY-MM-DD')%>") SORT file.mtime asc
LIMIT 5
```
