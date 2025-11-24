<%*
let type = await tp.system.suggester(["Blog Post", "Fiction", "Thought", "Other"], ["BLOG POSTS/", "FICTION/", "THOUGHTS/", "OTHER/"], true);
let title = await tp.system.prompt("Title", "", true);
let prefix = type == "THOUGHTS/" ? tp.date.now("YYYY-MM-DD_ddd") + " " : "";
await tp.file.move("PERSONAL/WRITING/" + type + prefix + title);
%>---
banner: "[[thought.jpg]]"
tags:
  - TODO/WRITE
---
# Daily Note : [[<%tp.date.now("YYYY-MM-DD_ddd")%>]]

---
