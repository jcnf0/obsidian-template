<%*
let title = await tp.system.prompt("Event Name", null, true);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.move("MISC/EVENTS/" + title.replace(invalidChars, ""));
%>---
banner: 
summary:
start_date:
end_date:
location:
tags:
---
# <% title %>

## Notes