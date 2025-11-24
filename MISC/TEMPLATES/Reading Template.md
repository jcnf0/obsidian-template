<%*
let type = await tp.system.suggester(["Book", "Other"], ["BOOKS/","OTHER/"], true);
let title = await tp.system.prompt("Title", null, true);
let author = await tp.system.prompt("Author", null, false);
let link = await tp.system.prompt("Link", null, false);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), false);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.move("PERSONAL/READING/" + type + title.replace(invalidChars, ""));
%>---
banner: "[[reading.png]]"
title: "<% title %>"
link: "<% link %>"
year: "<% year %>"
summary:
tags:
  - TODO/READ
---
# Daily Note : [[<%tp.date.now("YYYY-MM-DD_ddd")%>]]
---
# Notes