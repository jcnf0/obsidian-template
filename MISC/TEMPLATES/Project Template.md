<%*
let title = await tp.system.prompt("Project Title", null, true);
let year = await tp.system.prompt("Year", tp.date.now("YYYY"), false);

let collaborators_input = await tp.system.prompt(
  "Collaborators (comma-separated)",
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

let authors_yaml = parseList(collaborators_input);
let affiliations_yaml = parseList(affiliations_input);

const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(title.replace(invalidChars, ""));
%>---
title: <% title %>
year: <% year %>
collaborators:
<% authors_yaml %>
affiliations:
<% affiliations_yaml %>
context:
grants:
status: idea
tags:
---
# [[<% title %>]] 
## Overview / Abstract
==Provide a description of the project==

## Artifacts/Materials
==List all artifacts or materials related to the projects. This can include links to Overleaf, slides, accepted papers, etc.==

| Artifact | Link    | Note |
| -------- | ------- | ---- |
| Overleaf | ==N/A== |      |
| Paper    | ==N/A== |      |
| Code     | ==N/A== |      |
## Notes

## Quick Access
### Meetings
```dataview
TABLE daily_note as "Daily Note", summary AS "Summary"
FROM "RESEARCH/MEETINGS" where contains(projects, [[]])
SORT daily_note DESC
LIMIT 10
```

### Thoughts
```dataview
TABLE daily_note as "Daily Note", summary AS "Summary"
FROM "RESEARCH/WRITING/THOUGHTS" where contains(projects, [[]])
SORT daily_note DESC
LIMIT 10
```

### Papers
```dataview
TABLE daily_note as "Daily Note", summary AS "Summary"
FROM "RESEARCH/READING/PAPERS" where contains(projects, [[]])
SORT daily_note DESC
LIMIT 10
```
