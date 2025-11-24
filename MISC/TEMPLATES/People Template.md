---
company: 
location: 
title: 
email: <% await tp.system.prompt("Email", null, true) %>
website: <% await tp.system.prompt("Website", null, false) %>
aliases: 
---
[[People MOC]]
<%*
let name = await tp.system.prompt("Name", null, false);
await tp.file.rename(name)
%>
# <% name %>
---
# Meetings
```dataview
TABLE file.cday as Created, summary AS "Summary"
FROM "RESEARCH/MEETINGS" where contains(file.outlinks, [[]])
SORT file.cday DESC
```

# Notes