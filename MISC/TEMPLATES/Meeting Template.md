<%*
const invalidChars = /[:\/\\*?"<>|]/g;
const meeting_date_input = await tp.system.prompt("Meeting Date", tp.date.now("YYYY-MM-DD"), true);
const m = moment(meeting_date_input, "YYYY-MM-DD");
const meeting_date = m.format("YYYY-MM-DD");        // Dataview sort field
const meeting_date_link = m.format("YYYY-MM-DD_ddd"); // Daily note link
const meeting_year = m.format("YYYY");
const meeting_name = await tp.system.prompt("Meeting Name", "Meeting", true);
const safe_name = meeting_name.replace(invalidChars, "");
await tp.file.move(`RESEARCH/MEETINGS/${meeting_year}/${meeting_date_link} ${safe_name}`);
%>---
type: meeting
daily_note: <% meeting_date %>
context:
attendees:
summary:
projects:
tags:
---
# <% meeting_name %>
## Agenda

## Materials

---
## Notes