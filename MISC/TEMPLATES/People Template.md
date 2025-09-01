---
company: 
location: 
title: 
email: 
website: 
aliases: 
---
[[People MOC]]
# [[<% tp.file.title %>]]
<% await tp.file.move("/📖 RESEARCH/👥 MEETINGS/People/" + tp.file.title) %>

---
## Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "RESEARCH/MEETINGS" where contains(file.outlinks, [[]])
SORT file.cday DESC
```