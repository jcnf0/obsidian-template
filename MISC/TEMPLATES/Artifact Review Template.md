<%*
let title = await tp.system.prompt("Paper Title", null, true);
let link = await tp.system.prompt("Review Link", null, false);
let venue = await tp.system.prompt("Venue", null, true);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), true);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(venue + "'" + year.slice(-2) + " " + title.replace(invalidChars, ""))
%>---
banner: "code.webp"
type: "review"
title: "<% title %>"
link: "<% link %>"
venue: "<% venue %>"
year: <% year %>
daily_note: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - TODO/WRITE
---
# <% title %>




---
# Review
```
INSERT REVIEW TEMPLATE
```