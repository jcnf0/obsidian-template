<%* let name = await tp.system.prompt("Name", null, false);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(name.replace(invalidChars, "")); %>---
type: "affiliation"
website: <% await tp.system.prompt("Website", null, false) %>
aliases:
---
# [[<% name %>]] 

## People
```dataview
TABLE email as Email, website as Website 
FROM "MISC/PEOPLE" where contains(affiliations, [[]])
LIMIT 20
```