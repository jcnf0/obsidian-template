# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>
[[<% moment(tp.file.title,'YYYY-MM-DD_ddd').subtract(1, 'days').format("YYYY-MM-DD_ddd") %>|<< Yesterday]] | [[<% moment(tp.file.title,'YYYY-MM-DD_ddd').add(1, 'days').format("YYYY-MM-DD_ddd") %>|Tomorrow >>]]

---
# Weekly Note : [[{{date:gggg-[W]ww}}]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[review]` `BUTTON[thought]` `BUTTON[reading]`

---
## Scratch Pad


---
## Summary of Day


---
## Tasks
```tasks
scheduled {{date:YYYY-MM-DD}} OR done on {{date:YYYY-MM-DD}} 
limit 20
hide tags
hide due date
```
---
## Notes Created Today
```dataview
LIST FROM "CLASSES" OR "PERSONAL" OR "RESEARCH" WHERE file.cday = date("<%moment(tp.file.title,'YYYY-MM-DD').format('YYYY-MM-DD')%>") SORT file.ctime asc
LIMIT 5
```

## Notes Edited Today
```dataview
LIST FROM "CLASSES" OR "PERSONAL" OR "RESEARCH" WHERE file.mday = date("<%moment(tp.file.title,'YYYY-MM-DD').format('YYYY-MM-DD')%>") SORT file.mtime asc
LIMIT 5
```
