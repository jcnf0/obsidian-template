<%*
let type = await tp.system.suggester(["Research Thought", "Personal Thought", "Blog Post", "Fiction", "Other"], ["RESEARCH/WRITING/THOUGHTS/", "PERSONAL/WRITING/THOUGHTS/", "PERSONAL/WRITING/BLOG POSTS/", "PERSONAL/WRITING/FICTION/", "PERSONAL/WRITING/OTHER/"], true);
let title = await tp.system.prompt("Title", "", true);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.move(type + title.replace(invalidChars, ""));
%>---
banner: "writing.webp"
type: "writing"
summary:
daily_note: <% tp.date.now("YYYY-MM-DD") %>
projects:
tags:
  - TODO/WRITE
---
# <% title %>