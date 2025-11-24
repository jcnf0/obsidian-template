---
company:
summary:
tags:
---
<%*
let meeting_date = await tp.system.prompt("Meeting Date", tp.date.now("YYYY-MM-DD_ddd"), true);
let meeting_name = await tp.system.prompt("Meeting Name", "Meeting", true);
await tp.file.rename(meeting_date + " " + meeting_name);
%>[[Meetings MOC]]

# Daily Note : [[<%meeting_date%>]]
---
## Attendees

## Agenda

---
# Notes
- 
