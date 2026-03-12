<%*
let title = await tp.system.prompt("Title", null, true);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(title.replace(invalidChars, ""));
%>---
banner: "default.png"
title: "<% title %>"
daily_note: <% tp.date.now("YYYY-MM-DD") %>
tags:
---
# <% title %>