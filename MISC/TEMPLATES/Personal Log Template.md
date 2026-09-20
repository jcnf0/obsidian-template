<%*
const invalidChars = /[:\/\\*?"<>|]/g;
const m = moment(tp.date.now("YYYY-MM-DD"), "YYYY-MM-DD");
const date = m.format("YYYY-MM-DD"); // Dataview sort field
const log_date_link = m.format("YYYY-MM-DD_ddd"); // Daily note link
const log_year = m.format("YYYY");
await tp.file.move(`PERSONAL/LOGS/${log_year}/${log_date_link} Personal Log`);
%>---
type: log
daily_note: <% date %>
mood_rating:
summary:
tags:
  - TODO/WRITE
---
# <% log_date_link %> Personal Log