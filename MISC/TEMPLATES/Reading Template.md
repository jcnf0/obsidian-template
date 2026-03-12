<%*
let type = await tp.system.suggester(["Book", "Other"], ["BOOKS/","OTHER/"], true);
let title = await tp.system.prompt("Title", null, true);
let authors_input = await tp.system.prompt(
  "Authors (comma-separated)",
  "",
  false
);

const parseList = (input) =>
  input && input.trim().length > 0
    ? input
        .split(",")
        .map(v => `  - "[[${v.trim()}]]"`)
        .join("\n")
    : "  []";

let authors_yaml = parseList(authors_input);
let link = await tp.system.prompt("Link", null, false);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), false);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.move("PERSONAL/READING/" + type + title.replace(invalidChars, ""));
%>---
banner: "reading.png"
type: "reading"
title: "<% title %>"
link: "<% link %>"
year: <% year %>
authors:
<% authors_yaml %>
summary:
daily_note: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - TODO/READ
---
# <% title %>