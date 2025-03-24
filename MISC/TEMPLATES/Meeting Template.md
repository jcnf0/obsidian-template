---
date: <% tp.file.creation_date() %>
type: meeting
company: 
summary:
---
[[Meetings MOC]]
Date: [[<% tp.date.now("YYYY-MM-DD_ddd") %>]]
<% await tp.file.rename(tp.date.now("YYYY-MM-DD_ddd") + " " + tp.file.title) %>
# Daily Note : [[<%tp.date.now("YYYY-MM-DD_ddd")%>]]

---
## Attendees
- 

---
# Notes
- 