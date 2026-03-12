<%* let name = await tp.system.prompt("Name", null, false);
const invalidChars = /[:\/\\*?"<>|]/g;
await tp.file.rename(name.replace(invalidChars, "")); %>---
type: "person"
roles:
field:
affiliations:
position:
email: <% await tp.system.prompt("Email", null, true) %>
website: <% await tp.system.prompt("Website", null, false) %>
phone:
orcid:
scholar:
aliases:
---
# [[<% name %>]] 

## Related Projects
```dataview
TABLE year as Year, grants as Grants, status as Status 
FROM "RESEARCH/PROJECTS" where contains(collaborators, [[]])
SORT daily_note DESC
LIMIT 10
```
## Relationship Context
### Professional

### Personal

## Publications / Papers
```dataview
TABLE venue as Venue, year as Year, daily_note as "Daily Note" 
FROM "RESEARCH/READING/PAPERS" where contains(authors, [[]])
SORT daily_note DESC
LIMIT 10
```

## Meetings
```dataview
TABLE daily_note as "Daily Note", summary AS "Summary"
FROM "RESEARCH/MEETINGS" where contains(attendees, [[]])
SORT daily_note DESC
LIMIT 10
```
---
## Important Events

## Reflections