<%*
let title = await tp.system.prompt("Paper Title", null, true);
let link = await tp.system.prompt("Paper Link", null, false);
let venue = await tp.system.prompt("Venue", null, false);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), false);

let authors_input = await tp.system.prompt(
  "Authors (comma-separated)",
  "",
  false
);

let affiliations_input = await tp.system.prompt(
  "Affiliations (comma-separated)",
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
let affiliations_yaml = parseList(affiliations_input);

const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(title.replace(invalidChars, ""));
%>---
banner: "reading.png"
type: "paper"
title: "<% title %>"
link: "<% link %>"
venue: "<% venue %>"
year: <% year %>
summary:
daily_note: <% tp.date.now("YYYY-MM-DD") %>
authors:
<% authors_yaml %>
affiliations:
<% affiliations_yaml %>
projects:
tags:
  - TODO/READ
---
# <% title %>
## Abstract / Introduction

## Background

## Methodology

## Evaluation
