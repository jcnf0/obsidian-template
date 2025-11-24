<%*
let paper_title = await tp.system.prompt("Paper Title", null, true);
let link = await tp.system.prompt("Review Link", null, false);
let venue = await tp.system.prompt("Venue", null, true);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), true);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(venue + "'" + year.slice(-2) + " " + paper_title.replace(invalidChars, ""))
%>---
banner: "[[code.webp]]"
paper_title: "<% paper_title %>"
link: "<% link %>"
venue: "<% venue %>"
year: "<% year %>"
tags:
  - TODO/WRITE
---
[[Artifact Review MOC]]

# Daily Note : [[<%tp.date.now("YYYY-MM-DD_ddd")%>]]
---
# Notes




---
# Review
```
INSERT REVIEW TEMPLATE
```