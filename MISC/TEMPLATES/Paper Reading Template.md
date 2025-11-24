<%*
let paper_title = await tp.system.prompt("Paper Title", null, true);
let paper_link = await tp.system.prompt("Paper Link", null, false);
let venue = await tp.system.prompt("Venue", null, false);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), false);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(paper_title.replace(invalidChars, ""));
%>---
banner: "[[reading.png]]"
paper_title: "<% paper_title %>"
paper_link: "<% paper_link %>"
venue: "<% venue %>"
year: "<% year %>"
summary:
tags:
  - TODO/READ
---
[[Paper Reading MOC]]
# Daily Note : [[<%tp.date.now("YYYY-MM-DD_ddd")%>]]
---
# Notes
## Abstract / Introduction

## Background

## Methodology

## Evaluation
